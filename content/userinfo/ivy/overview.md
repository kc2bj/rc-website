+++
description = ""
title = "Ivy Secure Environment"
draft = false
date = "2020-02-14T11:45:12-05:00"
tags = ["ivy","vm","hipaa","linux","windows","security","jupyter","infrastructure"]
categories = ["userinfo"]
images = [""]
author = "RC Staff"  

+++

{{% callout %}}
<h4>Ivy</h4>

<p>Ivy is a secure computing environment for researchers consisting of virtual machines (Linux and Windows).
Researchers can use Ivy to process and store sensitive data with the confidence that the environment is secure and meets <a href="#hipaa-compliance">HIPAA or CUI requirements</a>.</p>

{{% /callout %}}

# Overview

Ivy consists of both virtual computing environments and secure storage. In order to obtain access to either system, users must **1. Submit an account request, 2. Complete the Information Security Awareness Training, and 3. Ensure their personal computer meets all High Security VPN requirements.**

* [Requesting Access](#requesting-access)
* [Training](#training)
* [High Security VPN](#high-security-vpn)
* [Virtual Machines](#virtual-machines)
* [JupyterLab Notebooks](#jupyterlab-notebooks)
* [Data Transfer In/Out of Ivy](#data-transfer-in-out-of-ivy)
* [HIPAA Compliance](#hipaa-compliance)

- - -

# Requesting Access

University of Virginia tenure stream and academic general faculty, research faculty, research scientists, and postdoctoral associates may request an account on Ivy. UVA graduate and undergraduate students are not permitted to request accounts—this must be done by their faculty advisor(s).

Access to Ivy resources is project-based, limited to PIs and their designees, and requires approval. Once a project is approved a PI and her/his researchers must sign a RUDA (one for every researcher on each project).

[<button class="btn btn-success">Request an Ivy Account</button>](https://services.rc.virginia.edu/ivyvm)

- - -

# Training

In order to use Ivy, researchers must complete the Information Security Awareness Training (ISAT). This training takes approximately 10 minutes to complete.

If you have a Workday account, please complete the training at the following link: <a href="https://www.myworkday.com/uva/d/inst/1$17816/17816$202.htmld" target="_blank">Workday ISAT</a>.

If you are a student and do not have a Workday account, please complete the training at this link instead: <a href="https://quiz.its.virginia.edu/itsa-staff" target="_blank">Student ISAT</a>.

- - -

# High Security VPN

The High Security VPN (HSVPN) allows researchers to connect to Ivy securely both on and off grounds. In order to use the HSVPN, users must ensure that their personal machines meet the following requirements. More information on HSVPN compliance can be found on the ITS website: <a href="https://in.virginia.edu/vpncheck" target="_blank">https://in.virginia.edu/vpncheck</a>

1. **Install the Cisco AnyConnect Secure Mobility Client.**
    This can be found at the <a href="https://virginia.service-now.com/its?id=sg_catalog&sys_id=d66f4fd4db29274c2192e665059619d6&sysparm_category=06d7db5bdbfcab00cebc550a48961963" target="_blank">UVA ITS Software Gateway</a>. Be sure to install the version of VPN Client HS 4.6 that is compatible with your personal computer's operating system. More detailed instructions for installing the VPN client can be found on the <a href="https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=f24e5cdfdb3acb804f32fb671d9619d0" target="_blank">ITS website</a>.
    
2. **Install Opswat.**
    Opswat checks if your computer is compliant with HSVPN requirements. Opswat can be downloaded from the <a href="https://virginia.service-now.com/its?id=sg_catalog&sys_id=a2bf4d91db716f402192e665059619fa" target="_blank">UVA ITS Software Gateway</a>.
    
3. **Install Anti-malware software (Cylance recommended)**.
    Anti-malware software must be installed on your machine. Cylance is behavioral-based antimalware software and meets UVA's HSVPN requirements. Cylance can downloaded from the <a href="https://virginia.service-now.com/its?id=sg_catalog&sys_id=b9fb6247db59270c2192e6650596190f" target="_blank">UVA ITS Software Gateway</a>.
    

<!-- 
# Pricing

Ivy resources will be provided without a fee for approved projects. Please note that the pricing model is still under evaluation. A valid PTAO is required as part of the account request process, although no charges will be made without advanced notice to the PI.

{{< ivy-pricing >}}
 -->

- - -

# Connecting and Signing In

## <span class="badge badge-default">1</span> Authentication

<div class="feature-box box">
  <p>You will sign in to all Ivy resources using your UVA computing ID and Eservices password. Because of Ivy's high security requirements, <b>your Eservices password must be changed every 60 days.</b></p>
  <p>Need help resetting your Eservices password?</p>
  <p><a href="https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=2f47ff87dbf6c744f032f1f51d961967" target="_new"><button class="btn btn-sm btn-warning">Reset Your Password</button></a></p>
  <p>If you are working from a secure Health Systems workstation you are ready to connect. If you are working from elsewhere on or off Grounds you will need Duo MFA and a High Security VPN connection.</p>
  </div>

## <span class="badge badge-default">2</span> Duo MFA

<div class="feature-box box">
  <img style="float:right;max-width:30%;" src="/images/duo-auth.png" alt="Duo 2-Factor Authentication" />
  <p>To connect to the Ivy environment with VPN you will need to install the Duo Mobile multi-factor authentication (MFA) app on your smartphone.</p>
  <ul>
    <li><a href="https://apps.apple.com/us/app/duo-mobile/id422663827" target="_new">Get Duo for iPhone in the App Store</a></li>
    <li><a href="https://play.google.com/store/apps/details?id=com.duosecurity.duomobile&hl=en_US" target="_new">Get Duo for Android on Google Play</a></li>
  </ul>
  <p>In the context of Ivy, Duo allows you two ways to provide a second factor of authentication beyond your password: via a random 6-digit key, or via a push message direct to your phone.</p>
  <a href="https://virginia.service-now.com/its?id=kb_article&sys_id=3c95c8d0dbc06f00f032f1f51d96191a" target="_new"><button class="btn btn-sm btn-warning">Set Up Duo</button></a>
</div>

## <span class="badge badge-default">3</span> High Security VPN

<div class="feature-box box">
  <p>With your UVA computing ID, Eservices password, and Duo Mobile in hand, you must run the Cisco AnyConnect software to start a UVA High Security VPN connection every time you use any Ivy resource. AnyConnect will authenticate to the UVA network using a digital certificate installed on your workstation. </p>
  <p>More information on VPN from ITS:</p>
  <ul>
    <li><a href="https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=9a5c088c6f59ee400a017f512e3ee4e2" target="_new">High Security VPN installation and connection instructions</a>.
    <li><a href="https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=58aafbcfdbf6c744f032f1f51d961927" target="_new">How to create, install, and use digital certificates</a>.
  </ul>
  <a href="https://virginia.service-now.com/its?id=itsweb_kb_article&sys_id=f24e5cdfdb3acb804f32fb671d9619d0" target="_new"><button class="btn btn-sm btn-warning">Learn More about UVA VPN</button></a>
</div>

Once you have completed these three steps, you will be connected to the secure Ivy network. From there you can connect to a Virtual Machine, or use a web browser to access JupyterLab.

- - -

# Virtual Machines

A virtual machine (VM) is a computing instance dedicated to your project. Multiple users can sign into a single VM.

Virtual machines come in two platforms, CentOS7 Linux and Windows Server 2012R2. Each platform is available in three instance types. Refer to the grid below for specifics.

{{% callout %}}
<p>Note that Windows VMs only support concurrent access by 2 users at a time.</p>

{{% /callout %}}


{{< ivy-pricing >}}

Once created, your instance will be assigned a private IP address that you will use to connect to it (in the format `10.xx.xx.xx`). VMs exist in a private, secure network and cannot
reach outside resources on the Internet. Most inbound and outbound data transfer is managed through the Data Transfer Node (see below).


## Connecting to your VM

To connect to your VM, you must install either an SSH client to connect to your VM using the command-line interface (CentOS VMs only), or
remote desktop software to connect to the desktop GUI of your VM. These options are outlined below.

**MacOSX Users:**

* Terminal (for SSH, built-in. Can be found in Applications -> Utilities -> Terminal)
* Microsoft Remote Desktop (for remote desktop to Windows or CentOS VMs, [download here](https://itunes.apple.com/us/app/microsoft-remote-desktop/id715768417?mt=12))

**Windows Users:**

* PuTTy (for SSH, [download here](http://www.chiark.greenend.org.uk/~sgtatham/putty/))
* Microsoft Remote Desktop (built-in, for remote desktop to Windows or CentOS VMs)


To connect to Ivy follow the platform-specific steps below:

<div class="row" style="margin-bottom:2rem;">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>CentOS 7 Linux</b>
      </div>
      <div class="card-block">
        <ul>
          <li>Open your High Security VPN connection</li>
          <li>Reference the IP address of your Ivy VM.</li>
          <li>For SSH access:<br />&nbsp;&nbsp;<code>ssh uva-id@ip-address</code></li>
          <li>For Remote Desktop access: Start the RDP client and point to the IP address of your VM and sign in.</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>Windows</b>
      </div>
      <div class="card-block">
        <ul>
          <li>Open your High Security VPN connection</li>
          <li>Reference the IP address of your Ivy VM.</li>
          <li>For Remote Desktop access: Start an RDP client and point to the IP address of your VM and sign in with your Eservices password and your computing ID prefixed by <em>ESERVICES</em> as the user name (i.e. <code>ESERVICES\mst3k</code>)</li>
        </ul>
      </div>
    </div>
  </div>
</div>


## Software

Every virtual machine (Linux or Windows) comes with a base installation of software by default. These help researchers by
providing the basic tools for data processing and manipulation. Additional software packages are pre-approved and available for installation
upon request. See the lists below for options.

### Preinstalled Software

<div class="row" style="margin-bottom:2rem;">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>PREINSTALLED Linux Software</b>
      </div>
      <div class="card-block">
        <i>Click on each for details:</i>
        <p class="card-text">
			{{% ivy-approved-software platform="Linux" installation="preinstalled" category="all" %}}
        </p>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>PREINSTALLED Windows Software</b>
      </div>
      <div class="card-block">
        <i>Click on each for details:</i>
        <p class="card-text">
			{{% ivy-approved-software platform="Windows" installation="preinstalled" category="all" %}}
        </p>
      </div>
    </div>
  </div>
</div>

**Python/R Packages** - Anaconda Python and R packages are available to users through the normal `pip`, `conda`, and `CRAN` and library installation methods.

### Additional Approved Software (Available by Request)

If you require additional software not listed, you must submit a request. Requests are reviewed by the UVA ISPRO office for security
and regulatory compliance and, if approved, will be installed for you.


<div class="row" style="margin-bottom:2rem;">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>ADDITIONAL Linux Groups</b>
      </div>
      <div class="card-block">
        <i>Click on each for more information:</i>
        <p class="card-text">
          <ul>
            <li><a href="/userinfo/ivy/ivy-linux-sw/overview" style="color: #0275d8;">All Packages</a></li>
            <li><a href="/userinfo/ivy/ivy-linux-sw/overview#bioinformatics" style="color: #0275d8;">Bioinformatics</a></li>
            <li><a href="/userinfo/ivy/ivy-linux-sw/overview#data-analysis" style="color: #0275d8;">Data Analysis</a></li>
            <li><a href="/userinfo/ivy/ivy-linux-sw/overview#image-processing" style="color: #0275d8;">Image Processing</a></li>
          </ul>
        </p>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-header">
        <b>ADDITIONAL Windows Groups</b>
      </div>
      <div class="card-block">
        <i>Click on each for more information:</i>
        <p class="card-text">
          <ul>
            <li><a href="/userinfo/ivy/ivy-windows-sw/overview" style="color: #0275d8;">All Packages</a></li>
            <li><a href="/userinfo/ivy/ivy-windows-sw/overview#bioinformatics" style="color: #0275d8;">Bioinformatics</a></li>
            <li><a href="/userinfo/ivy/ivy-windows-sw/overview#data-analysis" style="color: #0275d8;">Data Analysis</a></li>
            <li><a href="/userinfo/ivy/ivy-windows-sw/overview#image-processing" style="color: #0275d8;">Image Processing</a></li>
         </ul>
        </p>
      </div>
    </div>
  </div>
</div>

[<button class="btn btn-success">Software Details for Linux</button>](/userinfo/ivy/ivy-linux-sw/overview)
[<button class="btn btn-success">Software Details for Windows</button>](/userinfo/ivy/ivy-windows-sw/overview)
[<button class="btn btn-success">Request Ivy Software</button>](https://www.rc.virginia.edu/form/support-request)


## Storage

Ivy VM has a pool of over 2 petabytes of Network Attached Storage shared amongst users. A PI specifies the storage space s/he would like to have when requesting access to Ivy. Virtual machines do not come with any significant disk storage of their own.  

## Learn More

[<button class="btn btn-success">Read more about Ivy Virtual Machines</button>](https://discuss.rc.virginia.edu/c/ivy/vm)

- - -

# JupyterLab Notebooks

<div class="alert alert-danger">
  As of August 31, 2019 Domino Data Lab will no longer be available within Ivy. Existing projects should be migrated to a virtual machine.
  Interactive data sessions will be available using Jupyter Notebooks (coming soon!)
</div>

{{% callout %}}
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/1200px-Jupyter_logo.svg.png" align="right" style="max-width:20%;" />
JupyterLab is a web-based interactive development environment for Jupyter notebooks, code, and data. JupyterLab is flexible: configure and arrange the user interface to support a wide range of workflows in data science, scientific computing, and machine learning. JupyterLab is extensible and modular: write plugins that add new components and integrate with existing ones.
<br clear=all />
<a href="https://jupyter.org/" target="_new"><button class="btn btn-success">Learn more about Jupyter</button></a>
{{% /callout %}}

- - -

# Data Transfer In/Out of Ivy

Moving sensitive data into the Ivy VMware platform is possible through a secure Globus DTN (data transfer node). The Ivy DTN is connected to a pool of secure storage called “Ivy Central Storage” (ICS), which in turn is connected to Ivy VMs. Only active research projects using Ivy virtual machines can use this service.

<img style="max-width:100%;" alt="Ivy Secure DTN Flow" src="https://uvarc-discourse.s3.amazonaws.com/original/1X/95f8dfa70374a538d3e940dc69cf960d9e5ac9a6.png" />

## How to Connect to the DTN and Transfer Files

Before transferring files to Ivy, you will need Globus installed on the computer you are transferring data from. Globus can be downloaded from [https://www.globus.org/globus-connect-personal](https://www.globus.org/globus-connect-personal).

1. Ensure that you are **NOT** connected to the HSVPN. Data transfer will not work if you are connected to the HSVPN.

2. Open Globus in your web browser: [https://app.globus.org/file-manager](https://app.globus.org/file-manager). When logging in, select **University of Virginia** and log in with Netbadge.

3. Once you are in the Globus **File Manager**, select the two-panel view by clicking the two-panel button beside the **Panels** button in the top-right corner of the page. This should open a second panel on the page, so that you have two side by side.

4. In one panel, click on the **Collections** field and select your computer. You can then click to the directory that contains the data you want to move, or type the path to the directory in the **Path** field. Click the files or folders you want to transfer to select them.

5. In the remaining panel, click on the **Collections** field and search for and select the **Ivy Secure DTN**. Select the storage share to which you want to transfer data. (Unless you are part of multiple Ivy projects, you should only see one storage folder.)

6. Click the **Start** button beneath the first panel (should be highlighted) to begin the data transfer.

7. Once the data transfer is complete, you will be able to access the data in your VM by clicking the **ICS** shortcut on your VM's desktop.

- - -

# HIPAA Compliance

The Ivy platform is HIPAA compliant by design. From the <a href="https://research.virginia.edu/irb-hsr/protected-health-information-hipaa-regulations-and-research" target="_new">UVA Institutional Review Board for Health Sciences Research</a> (IRB-HSR):

<div class="bd-callout bd-callout-warning">
<p>HIPAA affects only that research which uses, creates, or discloses PHI. Researchers have legitimate needs to use, access, and disclose PHI to carry out a wide range of health research studies.</p>
<p>The Privacy Rule protects PHI while providing ways for researchers to access and use PHI when necessary to conduct research.</p>
<p>In general, there are two types of human research that would involve PHI:</p>

<ul>
<li>Studies involving review of existing medical records as a source of research information. Retrospective studies, such as chart reviews, often do this. Sometimes prospective studies do it also, for example, when they contact a participant's physician to obtain or verify some aspect of the participant's health history.
<li>Studies that create new medical information because a health care service is being performed as part of the research, such as testing of a new way of diagnosing a health condition or a new drug or device for treating a health condition. Virtually all sponsored clinical trials that submit data to the U.S. Food and Drug Administration (FDA) will involve PHI.
</ul>

</div>

Researchers must understand that, in general, the more difficult parts of HIPAA compliance are less technical (networks, computers, and data) than they are human and how users interact with these systems and data. The mishandling of data -- such as storing them on insecure devices or in insecure places -- jeopardizes confidential patient data and UVA's ability to remain a trusted keeper of those data.

All data imported into Ivy must be treated as highly sensitive data. Data and results exported from Ivy must be protected and managed appropriately according to UVA's [data classification guidelines](https://security.virginia.edu/university-data-protection-standards). Guidance regarding these guidelines and data types is available from UVA Information Security, Policy, and Records Office (ISPRO) by emailing [it-security@virginia.edu](it-security@virginia.edu).

<button onclick="topFunction()" id="scrollBtn" title="Go to top"><i class="fas fa-2x fa-angle-double-up"></i></button>


<!--

# Coming Soon - Secure HPC

<img src="https://pbs.twimg.com/media/DRQcamFX0AA9tmU.jpg" style="float:right;max-width:40%;" />

In 2019 we will launch a secure high performance computing system. This will support computationally-intensive research for sensitive data, within the Ivy secure environment.

-->

<br clear=all />