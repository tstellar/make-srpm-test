COPR_USERNAME=$(shell rpm --eval %copr_username)
COPR_PROJECT=$(shell rpm --eval %copr_projectname)

.phony: srpm

srpm:
	env
	dnf repolist
	cat $(outdir)/mock-source-build.cfg
	dnf install -y dnf-plugins-core
	dnf copr enable -y --setopt=reposdir=/tmp/yum.repos.d $COPR_USERNAME/$COPR_PROJECT
