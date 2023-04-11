1-Introdução aos comandos Commit
    Solução(){
        git commit;git commit
    }

1.2-Ramos no Git
    Solução(){
        git branch bugFix; git checkout bugFix;
    }

1.3-Branches e Merges
    Solução(){
        git branch bugFix; git checkout bugFix;
            git commit;git checkout main;
                git commit; git merge bugFix;
    }

1.4-Rebase no Git
    Solução(){
        git branch bugFix; git checkout bugFix;
            git commit;git checkout main;
                git commit; git checkout bugFix;
                    git rebase main
    }

1.5-Movendo-se no Git
    Solução(){
        git checkout C4;
    }

2-Referências relativas
    Solução(){
        git checkout bugFix; git checkout bugFix^;
    }

2.1-Referências relativas#2
    Solução(){
        git checkout C6; git branch -f bugFix HEAD~4;
            git branch -f main HEAD~0; git checkout C1;
    }

2.2-Revertendo Mudanças no Git
    Solução(){
        git reset HEAD~;git checkout pushed
            git revert C2;
    }

3-Movendo o trabalho por aí
    Solução(){
        git cherry-pick C3; git cherry-pick C4; git cherry-pick C7;
    }

3.1-Rebase Interativo do Git
    Solução(){
        git rebase -i HEAD~4;
    }

4-Commits empilhados localmente
    Solução(){
            git rebase -i HEAD~3;git branch -f main HEAD~0
    }

4.1-Malabarismo com commits
    Solução(){
        git rebase -i HEAD~2
            git commit --amend
                git rebase -i HEAD~2
                    git branch -f main HEAD~0
    }

4.2-Malabarismo com commits#2
    Solução(){
        git commit --amend;
            git checkout C2; git commit --amend;
                git commit --amend;git cherry-pirck C3;
                    git branch -f main HEAD~0; git checkout main;
    }

4.3-Tags no Git
    Solução(){
        git tag v1 C2; git tag v0 C1; git checkout C2;
    }

4.4-Git discribe
    Solução(){
        git commit;
    }

5.1-Fazendo mais de 9000 rebases
//Admito que para a solução desta, precisei ver o início do gabarito. Depois, consegui me guiar.
    Solução(){
    git rebase main bugFix;
        git rebase bugFix side;
            git rebase side another;
                git branch -f main HEAD~0; git checkout main;
    }

5.2-Multiplos pais
    Solução(){
        git branch bugWork C2;
    }

5.3-Espaguete de Ramos
    Solução(){
     git checkout C1;
        git cherry-pick C4 C3 C2;
            git checkout C1;
                git cherry-pick C5 C4 C3 C2;
                      git rebase C2' one;
                            git rebase C2 three;
                                git rebase c2'' two;

    }

6 - Introdução a clonagem
    Solução(){
        git clone;
    }

6.1 - Ramos Remotos no Git
    Solução(){
        git commit; git checkout o/main;
            git commit;
    }

6.2 - Git Fetch
    Solução(){
        git fetch;
    }

6.3 - Git pull
    Solução(){
        git pull;
    }

6.4 - Simulando colaboração
    Solução(){
        git clone;
            git fakeTeamwork main;
                git commit;
                    git pull;
    }

6.5- Git push
    Solução(){
        git commit; git commit;
            git push;
    }

6.6- Histórico Divergente
    Solução() {
        git clone; git fakeTeamwork;
            git commit; git pull --rebase;
                ;git push
    }

6.7- Main Bloqueado
    Solução() {
        git reset --hard o/main;
            git checkout -b feature C2;
                git push;
    }

7- Push main!
    Solução(){
         git rebase side1 side2;
            git rebase side2 side3;
                git rebase side3 main;
                    git pull --rebase;
                        git push;
    }

7.1-marge com remotos
    Solução(){
        git checkout main;git pull;
            git merge side1;git merge side2;
                git merge side3; git push
    }

7.2- Seguindo ramos remotos
    Solução(){
        git checkout -b side o/main;git commit;
            git pull --rebase;git push;
    }

7.3- Parâmetros do git push
    Solução(){
        git push origin main;git push origin foo;
    }

7.4-Parâmetros do git push -- expandido
    Solução(){
        git push origin main~1:foo;git push origin foo:main;

    }

7.5- Parâmetros do fetch
    Solução(){
        git fetch origin main~1:foo;git fetch origin foo:main;
            git checkout foo;git merge c6;
             }

7.6- Origem vazia
    Solução(){
        git push origin :foo; git fetch origin :bar;
    }

7.7- Parâmetros do pull
    Solução(){
        git pull origin bar:foo; git pull origin main:side
    }
