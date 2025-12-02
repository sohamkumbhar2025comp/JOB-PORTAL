# JOB-PORTAL
#include <stdio.h>

struct candidate{ char name[30],qualification[10];
                  int candidate_no,salary_expectation;
                  float experience;
                };

int main() {
    int n;
    printf("Enter number of candidates: ");
    scanf("%d", &n);
struct candidate c1[n];
     for(int i=0;i<n;i++){
         printf("\nCandidate %d details:\n", i + 1);
         printf("----------------------------------------------\n");
         printf("enter candidate name:");
         scanf("%s",&c1[i].name);
         printf("enter qualification(degree/education level):");
         scanf("%s",&c1[i].qualification);
         printf("enter experience:");
         scanf("%f",&c1[i].experience);
         printf("enter salary expectation:");
         scanf("%d",&c1[i].salary_expectation);
         printf("\n=============================================\n");
     }
     
for(int i = 0; i < n - 1; i++) {
               for(int j = 0; j < n - i - 1; j++) {
       if(c1[j].salary_expectation > c1[j + 1].salary_expectation) {
            struct candidate temp = c1[j];
            c1[j] = c1[j + 1];
            c1[j + 1] = temp;
        }
    }
}
 printf("Salary Expectation according to ascending order");
             for(int i=0;i<n;i++){
                 printf("\n%d. Candidate\n", i + 1);
                 printf("name:%s\n",c1[i].name);
                 printf("qualification:%s\n",c1[i].qualification);
                 printf("experience:%f\n",c1[i].experience);
                 printf("salary expectation:%d\n",c1[i].salary_expectation);
             }

  
return 0;
}
