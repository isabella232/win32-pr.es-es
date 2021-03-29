---
title: Instalación del proveedor
description: El procedimiento para instalar el proveedor WMI de DNS es distinto en función de la versión de Windows en la que está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nombres de dominio, proveedor WMI, instalar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774184"
---
# <a name="installing-the-provider"></a><span data-ttu-id="55a1f-104">Instalación del proveedor</span><span class="sxs-lookup"><span data-stu-id="55a1f-104">Installing the Provider</span></span>

<span data-ttu-id="55a1f-105">El procedimiento para instalar el proveedor WMI de DNS es distinto en función de la versión de Windows en la que está instalado.</span><span class="sxs-lookup"><span data-stu-id="55a1f-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="55a1f-106">En el procedimiento siguiente se describe cómo instalar y configurar el proveedor WMI de DNS en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="55a1f-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="55a1f-107">Para obtener el proveedor WMI de DNS para Windows 2000, descargue el siguiente archivo:</span><span class="sxs-lookup"><span data-stu-id="55a1f-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="55a1f-108">**ADVERTENCIA:** Los archivos del proveedor WMI de DNS no son intercambiables.</span><span class="sxs-lookup"><span data-stu-id="55a1f-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="55a1f-109">Los servidores DNS de Windows 2000 requieren diferentes archivos y un procedimiento diferente que los servidores DNS de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="55a1f-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="55a1f-110">Se proporciona el procedimiento para cada uno.</span><span class="sxs-lookup"><span data-stu-id="55a1f-110">The procedure for each is provided.</span></span>

<span data-ttu-id="55a1f-111">**Para instalar el proveedor WMI de DNS en el servidor de Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="55a1f-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="55a1f-112">Obtenga el proveedor WMI de DNS para Windows 2000 del kit de recursos del servidor de Windows 2000 o descargue el archivo, Dnsprov.zip, de: ftp://ftp.microsoft.com/reskit/win2000/</span><span class="sxs-lookup"><span data-stu-id="55a1f-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="55a1f-113">Copie los archivos del proveedor WMI de DNS (Dnsprov.dll) y Dnsschema. mof en el <winntdir> \\ \\ directorio system32 WBEM.</span><span class="sxs-lookup"><span data-stu-id="55a1f-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="55a1f-114">Compile el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="55a1f-114">Compile the MOF file.</span></span> <span data-ttu-id="55a1f-115">Al hacerlo, se personaliza el esquema para que coincida con el servidor.</span><span class="sxs-lookup"><span data-stu-id="55a1f-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="55a1f-116">**MOFCOMP Dnsschema. mof**</span><span class="sxs-lookup"><span data-stu-id="55a1f-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="55a1f-117">Registre el archivo DLL en el servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="55a1f-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="55a1f-118">**regsvr32 dnsprov.dll**</span><span class="sxs-lookup"><span data-stu-id="55a1f-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="55a1f-119">Los scripts o programas que utilizan el proveedor WMI de DNS para administrar los servidores DNS se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="55a1f-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="55a1f-120">Los scripts o programas se pueden ejecutar desde el servidor DNS o desde un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="55a1f-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="55a1f-121">El SDK de WMI no es necesario para ejecutar el proveedor WMI de DNS, pero contiene muchas herramientas útiles.</span><span class="sxs-lookup"><span data-stu-id="55a1f-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="55a1f-122">El proveedor WMI de DNS debe estar instalado en cualquier servidor DNS que se va a administrar; sin embargo, los scripts de DNS se pueden ejecutar en el servidor DNS o en un host remoto.</span><span class="sxs-lookup"><span data-stu-id="55a1f-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="55a1f-123">**Para instalar el proveedor WMI de DNS en Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="55a1f-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="55a1f-124">En el caso de los sistemas operativos Windows Server 2003, el proveedor WMI de DNS se instala y registra automáticamente, y su archivo MOF se compila cuando se instala el servicio servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="55a1f-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




