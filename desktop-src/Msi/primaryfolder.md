---
description: PRIMARYFOLDER es una propiedad global que permite al autor designar una carpeta principal para la instalación.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propiedad PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653463"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="ab5da-103">Propiedad PRIMARYFOLDER</span><span class="sxs-lookup"><span data-stu-id="ab5da-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="ab5da-104">**PRIMARYFOLDER** es una propiedad global que permite al autor designar una carpeta principal para la instalación.</span><span class="sxs-lookup"><span data-stu-id="ab5da-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="ab5da-105">El valor de esta propiedad debe ser el nombre de clave de un directorio que exista en la [tabla de directorios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5da-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="ab5da-106">El instalador usa la ruta de acceso resuelta de la carpeta principal para determinar qué volumen se debe usar al establecer los valores de la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) , la propiedad [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , la propiedad [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) y la propiedad [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5da-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="ab5da-107">El instalador proporciona los valores de estas últimas propiedades a los usuarios de la interfaz de usuario para ayudarles a administrar el espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ab5da-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="ab5da-108">Normalmente, los autores de paquetes pueden seleccionar la carpeta más grande que la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="ab5da-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="ab5da-109">El valor de esta propiedad debe ser el nombre de clave de un registro de directorio que se encuentra en la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5da-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5da-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab5da-110">Requirements</span></span>



| <span data-ttu-id="ab5da-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab5da-111">Requirement</span></span> | <span data-ttu-id="ab5da-112">Value</span><span class="sxs-lookup"><span data-stu-id="ab5da-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5da-113">Versión</span><span class="sxs-lookup"><span data-stu-id="ab5da-113">Version</span></span><br/> | <span data-ttu-id="ab5da-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ab5da-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ab5da-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab5da-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ab5da-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab5da-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ab5da-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ab5da-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab5da-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab5da-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5da-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab5da-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




