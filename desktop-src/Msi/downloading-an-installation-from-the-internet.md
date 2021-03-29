---
description: Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una instalación de.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Descarga de una instalación desde Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652535"
---
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="d62ed-103">Descarga de una instalación desde Internet</span><span class="sxs-lookup"><span data-stu-id="d62ed-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="d62ed-104">Windows Installer acepta un localizador uniforme de recursos (URL) como origen válido para una instalación de.</span><span class="sxs-lookup"><span data-stu-id="d62ed-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="d62ed-105">Windows Installer puede instalar paquetes, revisiones y transformaciones desde una ubicación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d62ed-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="d62ed-106">Si la base de datos de instalación se encuentra en una dirección URL, el instalador descarga la base de datos en una ubicación de caché antes de iniciar la instalación.</span><span class="sxs-lookup"><span data-stu-id="d62ed-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="d62ed-107">El instalador también descarga los archivos y archivos. cab desde el origen de Internet que son adecuados para las selecciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="d62ed-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="d62ed-108">Vea [un ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d62ed-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="d62ed-109">Por ejemplo, para instalar un paquete con un origen ubicado en un servidor Web en https://server/share/package.msi , puede utilizar las opciones de [línea de comandos](command-line-options.md) para instalar el paquete y establecer las propiedades [públicas](public-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="d62ed-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="d62ed-110">msiexec/i https://server/share/package.msi *Property = valor*</span><span class="sxs-lookup"><span data-stu-id="d62ed-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="d62ed-111">Se debe pasar al instalador una línea de comandos como la que se mostró anteriormente para iniciar una instalación desde un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="d62ed-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="d62ed-112">En general, no debe descargar e instalar el paquete simplemente haciendo doble clic en el archivo. msi desde el explorador.</span><span class="sxs-lookup"><span data-stu-id="d62ed-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="d62ed-113">Esto descarga el archivo. msi en la carpeta de archivos temporales de Internet y pasa el siguiente comando al instalador:</span><span class="sxs-lookup"><span data-stu-id="d62ed-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="d62ed-114">**msiexec/i c: \\ \\ archivos temporales de Internet de Windows \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="d62ed-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="d62ed-115">Se produce un error en la instalación si el paquete requiere archivos de origen o archivadores externos, ya que no se encuentran en la misma ubicación que el archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="d62ed-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="d62ed-116">Tenga en cuenta que, como el objeto de [**instalador**](installer-object.md) no está marcado como [SafeForScripting](safeforscripting.md) en el equipo del usuario, los usuarios deben ajustar la configuración de seguridad del explorador para que el ejemplo funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="d62ed-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="d62ed-117">El método [**InstallProduct**](installer-installproduct.md) se puede usar para ejecutar el comando anterior desde un explorador como un evento de clic.</span><span class="sxs-lookup"><span data-stu-id="d62ed-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="d62ed-118">Tenga en cuenta que, dado que algunos servidores web distinguen mayúsculas de minúsculas, el campo Nombre de archivo de la tabla de [archivos](file-table.md) debe coincidir exactamente con las mayúsculas y minúsculas de los archivos de origen para garantizar la compatibilidad con las descargas</span><span class="sxs-lookup"><span data-stu-id="d62ed-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="d62ed-119">Vea [Descargar e instalar una revisión desde Internet](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="d62ed-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="d62ed-120">Para obtener más información acerca de la protección de instalaciones y el uso de certificados digitales, consulte las [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="d62ed-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="d62ed-121">Para obtener más información sobre cómo crear una instalación Web de un paquete de Windows Installer, vea [arranque de descarga en Internet](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="d62ed-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="d62ed-122">Protocolos de Internet disponibles</span><span class="sxs-lookup"><span data-stu-id="d62ed-122">Available Internet Protocols</span></span>

<span data-ttu-id="d62ed-123">A partir de Windows Server 2003 y Windows XP, el instalador puede usar los protocolos HTTP, HTTPS y FILE.</span><span class="sxs-lookup"><span data-stu-id="d62ed-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="d62ed-124">El instalador no admite los protocolos FTP y GOPHER.</span><span class="sxs-lookup"><span data-stu-id="d62ed-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="d62ed-125">Windows Installer versión 2,0 puede usar los protocolos HTTP, archivo y FTP y no puede usar los protocolos HTTPS y GOPHER.</span><span class="sxs-lookup"><span data-stu-id="d62ed-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



