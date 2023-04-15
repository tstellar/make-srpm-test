.phony: srpm

srpm:
	env
	dnf repolist
	cat $(outdir)/mock-source-build.cfg
	dnf install -y dnf-plugins-core
	dnf copr enable -y --setopt=reposdir=/tmp/yum.repos.d `rpm --eval %copr_username`/`rpm --eval %copr_projectname`
  
