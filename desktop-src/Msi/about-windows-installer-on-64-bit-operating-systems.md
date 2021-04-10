---
description: Windows Installer se ejecuta como un servicio en equipos que usan Windows de 32 bits o de 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Acerca de Windows Installer en sistemas operativos de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "104279671"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="636ea-103">Acerca de Windows Installer en sistemas operativos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="636ea-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="636ea-104">Windows Installer se ejecuta como un servicio en equipos que usan Windows de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="636ea-105">Las versiones del instalador anteriores a la versión 2,0 solo pueden instalar y administrar paquetes de Windows Installer de 32 bits en sistemas operativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="636ea-106">Tenga en cuenta que no se puede anunciar ni instalar una aplicación de 64 bits en un sistema operativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="636ea-107">Un paquete de Windows Installer debe especificarse como un paquete de 32 bits o de 64 bits; no se puede especificar como neutral.</span><span class="sxs-lookup"><span data-stu-id="636ea-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="636ea-108">En un equipo que utiliza un sistema operativo de 64 bits, el servicio Windows Installer se hospeda en un proceso de 64 bits que instala los paquetes de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="636ea-109">Windows Installer instala tres tipos de paquetes de Windows Installer en un equipo que ejecuta un sistema operativo de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="636ea-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="636ea-110">paquetes de 32 bits que contienen solo componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="636ea-111">paquetes de 64 bits que contienen algunos componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="636ea-112">paquetes de 64 bits que contienen solo componentes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="636ea-113">En las secciones siguientes se describen los dos tipos de paquetes de Windows Installer y las nuevas propiedades de instalador proporcionadas por Windows Installer para los paquetes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="636ea-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="636ea-114">Paquetes de Windows Installer de bits de 32</span><span class="sxs-lookup"><span data-stu-id="636ea-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="636ea-115">Paquetes de Windows Installer de bits de 64</span><span class="sxs-lookup"><span data-stu-id="636ea-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="636ea-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="636ea-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636ea-117">Usar paquetes de Windows Installer de 64 bits</span><span class="sxs-lookup"><span data-stu-id="636ea-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



