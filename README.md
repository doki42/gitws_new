# Start, kell egy repó
1. git clone
  Már van egy remote repo, GitHub
  Clone esetén az adott mappában ahol kiadod a parancsot, ott csinál egy új mappát (a repó URL-jéből deriválva)
  SSH vagy HTTPS URL, kell az egyik
  SSH -> id_rsa
  HTTPS -> access token
  Ilyenkor "van remote kapcsolat", írd be, hogy "git remote -v" és látod honnan lett leklónozva
  Alapértelmezett "remote" neve az "origin"
2. git init
    Az adott mappából git repót csinál
    Ilyen esetben, nincs kapcsolat a lokális repód és egy "remote" közt
    Neked kell "remote-ot csinálni", mikor jó ez? Ha GitHub-on pl. csinálsz egy új üres repót (leírva a GitHub page, hogyan adsz hozzá a lokális repódhoz remote-ot)
3. Mitől git a repó git repó?
    A gyökérben van egy .git/ mappa
4. "fatal: not a git repository (or any of the parent directories): .git"
    Rossz helyen adod ki a git parancsot

# Local vs remote repository
1. Local - a te gépeden van
    A te gépeden létező verzió a repóból, de lehet több helyen is repó, pl. ha 6 ember együtt dolgozik akkor mindenkinek lesz egy lokális repója
2. Remote - az valaki más gépén van (GitHub, GitLab, BitBucket)
    Git != GitHub

# Történelem
* Mit lehet tárolni Gitben?
* VCS
* DVCS (Git)
* Linux kernelhez egy hogy kapcsolódik?

# Lingo
* verzió == commit, kommit 
* Side note SVN-ben így volt: revízió == revision
* hashcode == commit hash, pl. 98c7216549b9dff2c63fb74594209ac1715b9782
* Ez túl hosszú, viszont az eleje, az első 6-8 betű az kb. egyedi a bolygón, pl. 98c72165

# Git history
1. GitHub-on is nézhető "X commits" kicsi óra mellett
2. Terminálban a "git log" paranccsal

# Working
git clone
VS Code open folder (with embedded Git Bash terminál)
Írod a kódot
git status-t csekkolod sokszor, ez kiírja a repóban lévő fájlok állapotát
A fájloknak többféle állapota lehet
    1. Untracked
    1. Unmodified
    1. Modified/Deleted
    1. Staged
    1. Conflict
git status output-ok
    1. nothing to commit, working tree clean - nincs változtatás, semmilyen
    1. Changes not staged for commit - ezek azok a fájlok amiben van változtatás de nem jelölted meg, hogy beakarod committolni
    1. Changes to be committed - ezek azok a fájlok, amik megvannak jelölve, hogy commit-kor bekerüljenek egy új verzióba
git add fájlnév
git add . (ahol a pont a relatív referencia a munkakönyvtárra)
git rm
git commit output-ok
    1. no changes added to commit - nem volt semmit a "staging area"-ban amikor kiadtad a parancsot

# Git local sync with remote
git push
git pull (ez "git fetch" után "git merge")

# HF
* Klónozd le ezt: https://github.com/nocodb/nocodb
* Nézd meg a Git history-ját a terminálban :)
* git log-ból "q" ha túl hosszú a log
* git diff-et lessétek meg, ezzel lehet nézni fájlokban változást két commit között
* git reset
    1. git reset HEAD~1
    1. git reset HEAD~2
    1. git reset HEAD~3
