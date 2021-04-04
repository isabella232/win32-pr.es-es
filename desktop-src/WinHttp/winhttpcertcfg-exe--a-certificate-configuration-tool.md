---
description: La herramienta de configuración de certificados de los servicios HTTP de Microsoft Windows (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, permite a los administradores instalar y configurar certificados de cliente en cualquier almacén de certificados al que pueda tener acceso la cuenta del administrador de aplicaciones web (IWAM) del servidor de Internet. La herramienta también elimina la necesidad de hacer nada especial en cuentas como la cuenta IWAM para obtener acceso a los certificados cuando se utiliza Active Server páginas (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, una herramienta de configuración de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154313"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="a89a5-104">WinHttpCertCfg.exe, una herramienta de configuración de certificados</span><span class="sxs-lookup"><span data-stu-id="a89a5-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="a89a5-105">La herramienta de configuración de certificados de los [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", permite a los administradores instalar y configurar certificados de cliente en cualquier [*almacén de certificados*](glossary.md) al que pueda tener acceso la cuenta del administrador de aplicaciones web (IWAM) del servidor de Internet.</span><span class="sxs-lookup"><span data-stu-id="a89a5-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="a89a5-106">La herramienta también elimina la necesidad de hacer nada especial en cuentas como la cuenta IWAM para obtener acceso a los certificados cuando se utiliza Active Server páginas (ASP).</span><span class="sxs-lookup"><span data-stu-id="a89a5-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="a89a5-107">Microsoft Management Console (MMC) permite a los administradores importar certificados de cliente en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="a89a5-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="a89a5-108">Sin embargo, la importación de un certificado no concede automáticamente acceso a la clave privada para otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="a89a5-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="a89a5-109">Esta clave privada es necesaria para la autenticación de certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="a89a5-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="a89a5-110">La herramienta de configuración de certificados de los servicios HTTP de Microsoft Windows (WinHTTP) proporciona la capacidad de conceder acceso a cuentas adicionales, como la cuenta IWAM, cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a89a5-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="a89a5-111">Uso de la herramienta de configuración de certificados</span><span class="sxs-lookup"><span data-stu-id="a89a5-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="a89a5-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a89a5-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="a89a5-113">Uso de la herramienta de configuración de certificados</span><span class="sxs-lookup"><span data-stu-id="a89a5-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="a89a5-114">La herramienta de configuración de certificados WinHTTP, WinHttpCertCfg.exe, está disponible como descarga en el sitio web de [herramientas del kit de recursos de Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="a89a5-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="a89a5-115">En el ejemplo de código siguiente se muestran los parámetros de línea de comandos válidos para usar con esta herramienta.</span><span class="sxs-lookup"><span data-stu-id="a89a5-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="a89a5-116">En la tabla siguiente se enumeran los parámetros de la herramienta de configuración de.</span><span class="sxs-lookup"><span data-stu-id="a89a5-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a89a5-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a89a5-117">Parameter</span></span></th>
<th><span data-ttu-id="a89a5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a89a5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a89a5-119">-?</span><span class="sxs-lookup"><span data-stu-id="a89a5-119">-?</span></span></td>
<td><span data-ttu-id="a89a5-120">Muestra datos de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="a89a5-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a89a5-121">-i</span><span class="sxs-lookup"><span data-stu-id="a89a5-121">-i</span></span></td>
<td><span data-ttu-id="a89a5-122">Especifica que el certificado se va a importar desde un archivo de intercambio de información personal (PFX).</span><span class="sxs-lookup"><span data-stu-id="a89a5-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="a89a5-123">Este parámetro debe ir seguido del nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="a89a5-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="a89a5-124">Cuando se especifica este parámetro, &quot; &quot; &quot; &quot; también se deben especificar-a y-c.</span><span class="sxs-lookup"><span data-stu-id="a89a5-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a89a5-125">-g</span><span class="sxs-lookup"><span data-stu-id="a89a5-125">-g</span></span></td>
<td><span data-ttu-id="a89a5-126">Especifica que se concede acceso a una clave privada.</span><span class="sxs-lookup"><span data-stu-id="a89a5-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="a89a5-127">Cuando se especifica este parámetro, &quot; &quot; &quot; también se deben especificar-a,-c &quot; y &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="a89a5-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a89a5-128">-r</span><span class="sxs-lookup"><span data-stu-id="a89a5-128">-r</span></span></td>
<td><span data-ttu-id="a89a5-129">Especifica que se quita el acceso para una clave privada.</span><span class="sxs-lookup"><span data-stu-id="a89a5-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="a89a5-130">Cuando se especifica este parámetro, &quot; &quot; &quot; también se deben especificar-a,-c &quot; y &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="a89a5-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a89a5-131">-l</span><span class="sxs-lookup"><span data-stu-id="a89a5-131">-l</span></span></td>
<td><span data-ttu-id="a89a5-132">Especifica que se enumeran las cuentas con acceso a una clave privada.</span><span class="sxs-lookup"><span data-stu-id="a89a5-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="a89a5-133">Cuando se especifica este parámetro, &quot; &quot; &quot; &quot; también se deben especificar-c y-s.</span><span class="sxs-lookup"><span data-stu-id="a89a5-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a89a5-134">-a</span><span class="sxs-lookup"><span data-stu-id="a89a5-134">-a</span></span></td>
<td><span data-ttu-id="a89a5-135">Especifica la cuenta de usuario en la máquina que se está configurando.</span><span class="sxs-lookup"><span data-stu-id="a89a5-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="a89a5-136">Puede ser una cuenta de dominio o de equipo local, como &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; o &quot; TESTDOMAIN\DOMAINUSER &quot; .</span><span class="sxs-lookup"><span data-stu-id="a89a5-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a89a5-137">-c</span><span class="sxs-lookup"><span data-stu-id="a89a5-137">-c</span></span></td>
<td><span data-ttu-id="a89a5-138">Especifica la ubicación y el nombre del <a href="glossary.md"><em>almacén de certificados</em></a>.</span><span class="sxs-lookup"><span data-stu-id="a89a5-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="a89a5-139">Utilice &quot; LOCAL_MACHINE &quot; o &quot; CURRENT_USER &quot; para designar qué rama del registro se va a usar para la ubicación.</span><span class="sxs-lookup"><span data-stu-id="a89a5-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="a89a5-140">El <em>almacén de certificados</em> puede estar instalado en la máquina.</span><span class="sxs-lookup"><span data-stu-id="a89a5-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="a89a5-141">Los ejemplos de nombre típicos son &quot; My &quot; , &quot; root &quot; y &quot; TrustedPeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="a89a5-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="a89a5-142">La ubicación y el nombre del <em>almacén de certificados</em> se separan con una barra diagonal inversa, por ejemplo, &quot; LOCAL_MACHINE \root &quot; .</span><span class="sxs-lookup"><span data-stu-id="a89a5-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a89a5-143">Aunque se &quot; &quot; puede especificar la rama CURRENT_USER del registro con este parámetro, la extensión del acceso a las claves privadas está pensada principalmente para los certificados instalados en un <a href="glossary.md"><em>almacén de certificados</em></a> del equipo local al que pueden tener acceso varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="a89a5-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a89a5-144">-S</span><span class="sxs-lookup"><span data-stu-id="a89a5-144">-s</span></span></td>
<td><span data-ttu-id="a89a5-145">Especifica una cadena de búsqueda que no distingue entre mayúsculas y minúsculas para buscar el primer certificado enumerado con un nombre de sujeto que contiene esta subcadena.</span><span class="sxs-lookup"><span data-stu-id="a89a5-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a89a5-146">-p</span><span class="sxs-lookup"><span data-stu-id="a89a5-146">-p</span></span></td>
<td><span data-ttu-id="a89a5-147">Especifica una contraseña que se usa para importar el certificado y la clave privada.</span><span class="sxs-lookup"><span data-stu-id="a89a5-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="a89a5-148">Solo se usa con la opción de importación.</span><span class="sxs-lookup"><span data-stu-id="a89a5-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="a89a5-149">El usuario debe tener privilegios suficientes para usar esta herramienta, que requiere que el usuario sea un administrador y el mismo usuario que instaló el certificado de cliente, si está instalado.</span><span class="sxs-lookup"><span data-stu-id="a89a5-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="a89a5-150">La herramienta "WinHttpCertCfg.exe" no es útil para configurar certificados almacenados en un sistema de archivos como FAT32, que no admite listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="a89a5-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="a89a5-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a89a5-151">Examples</span></span>

<span data-ttu-id="a89a5-152">En los ejemplos siguientes se muestran algunas de las formas en que se puede usar la herramienta de configuración.</span><span class="sxs-lookup"><span data-stu-id="a89a5-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="a89a5-153">Este comando muestra las cuentas que tienen acceso a la clave privada para el certificado "percertificate" en el [*almacén de certificados*](glossary.md) "raíz" de la \_ rama del equipo local del registro.</span><span class="sxs-lookup"><span data-stu-id="a89a5-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="a89a5-154">**winhttpcertcfg-l-c raíz de la \_ máquina local \\ -s-certificado**</span><span class="sxs-lookup"><span data-stu-id="a89a5-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="a89a5-155">Este comando concede acceso a la clave privada del certificado "mi certificado" en el [*almacén de certificados*](glossary.md) "mi" para la cuenta usuarioDePrueba.</span><span class="sxs-lookup"><span data-stu-id="a89a5-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="a89a5-156">**winhttpcertcfg-g-c \_ equipo local \\ My-s mi certificado-a TESTUSER**</span><span class="sxs-lookup"><span data-stu-id="a89a5-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="a89a5-157">Este comando importa un certificado y una clave privada de un archivo PFX y extiende el acceso a la clave privada a otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="a89a5-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="a89a5-158">**winhttpcertcfg-i PFXFile-c \_ equipo local \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**</span><span class="sxs-lookup"><span data-stu-id="a89a5-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="a89a5-159">Este comando deniega el acceso a la clave privada de la \_ cuenta de IWAM TESTMACHINE con el certificado especificado.</span><span class="sxs-lookup"><span data-stu-id="a89a5-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="a89a5-160">**winhttpcertcfg-r-c \_ raíz del equipo local \\ -s-certificado-a IWAM \_ TESTMACHINE**</span><span class="sxs-lookup"><span data-stu-id="a89a5-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




