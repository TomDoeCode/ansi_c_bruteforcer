#include <stdio.h>
#include <string.h>
#include <stdlib.h>

#define MAX_LENGTH 4
#define CHAR_SET "abcdefghijklmnopqrstuvwxyz0123456789"

int passwordFound = 0;

void bruteforce(char *current, int position, const char *target) {
    if (passwordFound) return;

    if (position == MAX_LENGTH) {
        current[position] = '\0';
        if (strcmp(current, target) == 0) {
            printf("\nPasswort gefunden: %s\n", current);
            passwordFound = 1;
        }
        return;
    }

    for (int i = 0; i < strlen(CHAR_SET); i++) {
            if (passwordFound) return;

        current[position] = CHAR_SET[i];
        current[position + 1] = '\0';
        printf("\rPruefe: %s", current);
        fflush(stdout);
        bruteforce(current, position + 1, target);
        }
    }

    void waitForKeyPress() {
    printf("\nDrueckenSie eine beliebige Taste, um das Programm zu beenden...\n");
    getchar();
    getchar();
    }


    int main() {
        char targetPassword[MAX_LENGTH + 1];
        char current[MAX_LENGTH + 1];

        printf("Bitte geben Sie ein Passwort (nur kleine Buchstaben) mit Maximal %d Zeichen (inklusive Zahlen) ein: ", MAX_LENGTH);
        scanf("%4s", targetPassword);

        printf("Starte Bruteforce....\n\n");
        bruteforce(current, 0, targetPassword);

        waitForKeyPress();

        return 0;
        }
