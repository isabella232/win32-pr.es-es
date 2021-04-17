---
description: Al establecer la propiedad TRANSFORMSSECURE en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propiedad TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681117"
---
# <a name="transformssecure-property"></a><span data-ttu-id="18044-103">Propiedad TRANSFORMSSECURE</span><span class="sxs-lookup"><span data-stu-id="18044-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="18044-104">Al establecer la propiedad **TRANSFORMSSECURE** en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="18044-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="18044-105">Establecer esta propiedad es como establecer la [Directiva TransformsSecure](transformssecure-policy.md) , salvo que el ámbito es diferente.</span><span class="sxs-lookup"><span data-stu-id="18044-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="18044-106">La configuración de la Directiva TransformsSecure se aplica a todos los paquetes instalados por un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="18044-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="18044-107">El establecimiento de la propiedad **TRANSFORMSSECURE** se aplica al paquete independientemente del usuario.</span><span class="sxs-lookup"><span data-stu-id="18044-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="18044-108">El propósito de esta propiedad es proporcionar almacenamiento de transformación seguro con usuarios móviles de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="18044-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="18044-109">Cuando se establece esta propiedad, una [instalación de mantenimiento](maintenance-installation.md) solo puede utilizar la transformación de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="18044-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="18044-110">Si la ruta de acceso no está disponible, se produce un error en la instalación del mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="18044-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="18044-111">Por tanto, un origen para cada transformación segura debe residir en la ubicación del origen del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="18044-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="18044-112">Después, si el instalador detecta que falta la transformación en el equipo local, puede restaurar la transformación desde este origen.</span><span class="sxs-lookup"><span data-stu-id="18044-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="18044-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18044-113">Remarks</span></span>

<span data-ttu-id="18044-114">Windows Installer interpreta la propiedad [**TRANSFORMSATSOURCE**](transformsatsource.md) para que sea igual que la propiedad **TRANSFORMSSECURE** .</span><span class="sxs-lookup"><span data-stu-id="18044-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="18044-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18044-115">Requirements</span></span>



| <span data-ttu-id="18044-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18044-116">Requirement</span></span> | <span data-ttu-id="18044-117">Value</span><span class="sxs-lookup"><span data-stu-id="18044-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18044-118">Versión</span><span class="sxs-lookup"><span data-stu-id="18044-118">Version</span></span><br/> | <span data-ttu-id="18044-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="18044-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="18044-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="18044-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="18044-121">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18044-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="18044-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="18044-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18044-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18044-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18044-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="18044-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="18044-125">Transformaciones de base de datos</span><span class="sxs-lookup"><span data-stu-id="18044-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




