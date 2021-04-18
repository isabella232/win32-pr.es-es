---
title: Ejemplos de capas de canales de seguridad
description: En los siguientes ejemplos se muestra la seguridad en la capa del canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- ejemplos de seguridad
- ejemplos de seguridad, configuración
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704713"
---
# <a name="security-channel-layer-examples"></a><span data-ttu-id="f11de-107">Ejemplos de capas de canales de seguridad</span><span class="sxs-lookup"><span data-stu-id="f11de-107">Security Channel Layer Examples</span></span>

<span data-ttu-id="f11de-108">En los siguientes ejemplos se muestra la seguridad en el [nivel de canal](channel-layer-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="f11de-108">The following examples illustrate security in the [Channel Layer](channel-layer-overview.md)</span></span>

<span data-ttu-id="f11de-109">Seguridad de transporte de Windows a través de TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-109">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="f11de-110">Seguridad de transporte de Windows a través de canalizaciones con nombre: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-110">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="f11de-111">Seguridad de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-111">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="f11de-112">Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-112">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="f11de-113">Nombre de usuario sobre SSL en modo mixto: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-113">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

<span data-ttu-id="f11de-114">Nombre de usuario sobre la seguridad de modo mixto de SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-114">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="f11de-115">Token emitido sobre seguridad de modo mixto de SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-115">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="f11de-116">Certificado X509 sobre seguridad de modo mixto de SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-116">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="one-time-setup-for-security-samples"></a><span data-ttu-id="f11de-117">One-Time el programa de instalación de ejemplos de seguridad</span><span class="sxs-lookup"><span data-stu-id="f11de-117">One-Time Setup for Security Samples</span></span>

<span data-ttu-id="f11de-118">Para ejecutar ejemplos de seguridad de WWSAPI, debe configurar los certificados de cliente y de servidor para SSL, así como una cuenta de usuario local para la autenticación de encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="f11de-118">To run WWSAPI security examples, you need to set up the client and server certificates for SSL, as well as a local user account for HTTP header authentication.</span></span> <span data-ttu-id="f11de-119">Antes de empezar, necesita las siguientes herramientas:</span><span class="sxs-lookup"><span data-stu-id="f11de-119">Before you start, you need the following tools:</span></span>

-   <span data-ttu-id="f11de-120">MakeCert.exe (disponible en el SDK de Windows 7).</span><span class="sxs-lookup"><span data-stu-id="f11de-120">MakeCert.exe (Available in the Windows 7 SDK.)</span></span>
-   <span data-ttu-id="f11de-121">CertUtil.exe o CertMgr.exe (CertUtil.exe está disponible en los SDK de Windows a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f11de-121">CertUtil.exe or CertMgr.exe (CertUtil.exe is available in the Windows SDKs starting with Windows Server 2003.</span></span> <span data-ttu-id="f11de-122">CertMgr.exe está disponible en el SDK de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f11de-122">CertMgr.exe is available in the Windows 7 SDK.</span></span> <span data-ttu-id="f11de-123">Solo se necesita una de estas herramientas).</span><span class="sxs-lookup"><span data-stu-id="f11de-123">You only need one of these tools.)</span></span>
-   <span data-ttu-id="f11de-124">HttpCfg.exe: (solo es necesario si usa Windows 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f11de-124">HttpCfg.exe: (You need this only if you are using Windows 2003 or Windows XP.</span></span> <span data-ttu-id="f11de-125">Esta herramienta está disponible en las herramientas de soporte de Windows XP SP2 y también se incluye en el CD de herramientas del kit de recursos de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f11de-125">This tool is available in Windows XP SP2 Support Tools and also comes with the Windows Server 2003 Resource Kit Tools CD.)</span></span>

<span data-ttu-id="f11de-126">Si obtiene los ejemplos de WWSAPI instalando el SDK de Windows 7, puede encontrar los MakeCert.exe y CertMgr.exe en% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="f11de-126">If you get the WWSAPI examples by installing the Windows 7 SDK, you can find the MakeCert.exe and CertMgr.exe under %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\bin.</span></span>

<span data-ttu-id="f11de-127">Realice la siguiente configuración en cinco pasos desde el símbolo del sistema (elevado si usa Windows Vista y versiones posteriores):</span><span class="sxs-lookup"><span data-stu-id="f11de-127">Perform the following five-step setup from the command prompt (elevated if you are using Windows Vista and above):</span></span>

1.  <span data-ttu-id="f11de-128">Genere un certificado autofirmado para que sea la entidad de certificación (CA) o el emisor: **MakeCert.exe-SS root-Sr LocalMachine-n "CN = falsificate-test-CA"-CY Authority-r-SK "CAKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="f11de-128">Generate a self-signed certificate to be the certificate authority (CA) or issuer: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**</span></span>
2.  <span data-ttu-id="f11de-129">Genere un certificado de servidor con el certificado anterior como emisor: **MakeCert.exe-SS My-Sr LocalMachine-n "CN = localhost"-Sky Exchange-is root-ir LocalMachine-in falsificate-test-CA-SK "ServerKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="f11de-129">Generate a server certificate using the previous certificate as the issuer: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**</span></span>
3.  <span data-ttu-id="f11de-130">Busque la huella digital (un hash SHA-1 de 40 caracteres) del certificado de servidor mediante la ejecución de cualquiera de los siguientes comandos y busque el certificado denominado localhost con el emisor falso-test-CA:</span><span class="sxs-lookup"><span data-stu-id="f11de-130">Find the thumbprint (a 40-character SHA-1 hash) of the server certificate by running either of the following commands and search for the certificate named localhost with issuer Fake-Test-CA:</span></span>
    -   <span data-ttu-id="f11de-131">**CertUtil.exe: almacenar mi localhost**</span><span class="sxs-lookup"><span data-stu-id="f11de-131">**CertUtil.exe -store My localhost**</span></span>
    -   <span data-ttu-id="f11de-132">**CertMgr.exe-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="f11de-132">**CertMgr.exe -s -r LocalMachine My**</span></span>
4.  <span data-ttu-id="f11de-133">Registre la huella digital del certificado de servidor sin espacios con HTTP.SYS:</span><span class="sxs-lookup"><span data-stu-id="f11de-133">Register the server certificate?s thumbprint with no spaces with HTTP.SYS:</span></span>
    -   <span data-ttu-id="f11de-134">En Windows Vista y versiones posteriores (la opción "AppID" es un GUID arbitrario): **Netsh.exe http Add sslcert ipport = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint></span><span class="sxs-lookup"><span data-stu-id="f11de-134">On Windows Vista and above (the "appid" option is an arbitrary GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint></span></span>
    -   <span data-ttu-id="f11de-135">En Windows XP o 2003: **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**</span><span class="sxs-lookup"><span data-stu-id="f11de-135">On Windows XP or 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**</span></span>
5.  <span data-ttu-id="f11de-136">Cree un usuario local: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**</span><span class="sxs-lookup"><span data-stu-id="f11de-136">Create a local user: **Net user "TestUserForBasicAuth" "TstPWD@\*4Bsic" /add**</span></span>

<span data-ttu-id="f11de-137">Para limpiar los certificados, el enlace de certificado SSL y la cuenta de usuario creada en los pasos anteriores, ejecute los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="f11de-137">To clean up the certificates, SSL certificate binding and the user account created in the previous steps, run the following commands.</span></span> <span data-ttu-id="f11de-138">Nota: si hay varios certificados con el mismo nombre, CertMgr.exe necesitará la entrada antes de eliminarlos.</span><span class="sxs-lookup"><span data-stu-id="f11de-138">Note if there are multiple certificates of the same name, CertMgr.exe will need your input before deleting them.</span></span>

-   <span data-ttu-id="f11de-139">**CertMgr.exe-del-c-n Falsificate-test-CA-s-r LocalMachine raíz**</span><span class="sxs-lookup"><span data-stu-id="f11de-139">**CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**</span></span>
-   <span data-ttu-id="f11de-140">**CertMgr.exe-del-c-n localhost-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="f11de-140">**CertMgr.exe -del -c -n localhost -s -r LocalMachine My**</span></span>
-   <span data-ttu-id="f11de-141">**Netsh.exe http Delete sslcert ipport = 0.0.0.0:8443 (o HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**</span><span class="sxs-lookup"><span data-stu-id="f11de-141">**Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (or HttpCfg.exe delete ssl -i 0.0.0.0:8443)**</span></span>
-   <span data-ttu-id="f11de-142">**Net user "TestUserForBasicAuth"/Delete**</span><span class="sxs-lookup"><span data-stu-id="f11de-142">**Net user "TestUserForBasicAuth" /delete**</span></span>

<span data-ttu-id="f11de-143">Asegúrese de que solo hay un certificado raíz denominado falso-test-CA.</span><span class="sxs-lookup"><span data-stu-id="f11de-143">Make sure there is only one root certificate named Fake-Test-CA.</span></span> <span data-ttu-id="f11de-144">Si no está seguro, es siempre seguro que intente limpiar estos certificados con los comandos de limpieza anteriores (y omitir los errores) antes de iniciar la configuración de cinco pasos.</span><span class="sxs-lookup"><span data-stu-id="f11de-144">If you are unsure, it?s always safe to try to clean up these certificates using the cleanup commands above (and ignore errors) before starting the five-step setup.</span></span>

 

 




