---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Las subclaves y los valores del registro asociados a la \_ clave HKEY local \_ Machine \\ software \\ classes contienen información sobre una aplicación que es necesaria para admitir la funcionalidad com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779633"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="f9859-103">HKEY \_ \_ clases de \\ software de máquina local \\</span><span class="sxs-lookup"><span data-stu-id="f9859-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="f9859-104">Las subclaves y los valores del registro asociados a la clave **HKEY \_ local \_ Machine \\ software \\ classes** contienen información sobre una aplicación que es necesaria para admitir la funcionalidad com.</span><span class="sxs-lookup"><span data-stu-id="f9859-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="f9859-105">Esta información incluye temas como formatos de datos admitidos, información de compatibilidad, identificadores de programación, DCOM y controles.</span><span class="sxs-lookup"><span data-stu-id="f9859-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="f9859-106">Subclave</span><span class="sxs-lookup"><span data-stu-id="f9859-106">Subkey</span></span>                                                                         | <span data-ttu-id="f9859-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9859-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9859-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="f9859-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="f9859-109">Opciones de configuración para aplicaciones basadas en COM.</span><span class="sxs-lookup"><span data-stu-id="f9859-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="f9859-110">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="f9859-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="f9859-111">Opciones de configuración para las clases COM.</span><span class="sxs-lookup"><span data-stu-id="f9859-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="f9859-112">**<extensión de archivo \_>**</span><span class="sxs-lookup"><span data-stu-id="f9859-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="f9859-113">Asocia una extensión de nombre de archivo a un ProgID.</span><span class="sxs-lookup"><span data-stu-id="f9859-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="f9859-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="f9859-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="f9859-115">Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para comparar patrones con distintos bytes de archivo en un archivo no compuesto.</span><span class="sxs-lookup"><span data-stu-id="f9859-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="f9859-116">**Interfaz**</span><span class="sxs-lookup"><span data-stu-id="f9859-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="f9859-117">Asocia un nombre de interfaz a un identificador de interfaz (IID).</span><span class="sxs-lookup"><span data-stu-id="f9859-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="f9859-118">Identifica una clase.</span><span class="sxs-lookup"><span data-stu-id="f9859-118">Identifies a class.</span></span> <span data-ttu-id="f9859-119">Tenga en cuenta que no se garantiza que el ProgID sea único globalmente, a diferencia de un CLSID.</span><span class="sxs-lookup"><span data-stu-id="f9859-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="f9859-120">**ProgID independiente de la versión de<>**</span><span class="sxs-lookup"><span data-stu-id="f9859-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="f9859-121">Se utiliza para determinar la versión más reciente de una aplicación de objeto.</span><span class="sxs-lookup"><span data-stu-id="f9859-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




