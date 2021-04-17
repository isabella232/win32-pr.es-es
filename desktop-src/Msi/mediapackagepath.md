---
description: 'Si el paquete de instalación que se envía con una aplicación no se encuentra en la raíz del CD-ROM que reciben los clientes, la propiedad MEDIAPACKAGEPATH debe establecerse en la línea de comandos para la ruta de acceso relativa de la aplicación en el CD-ROM. Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ mypath \\My.msi, use MEDIAPACKAGEPATH =&\# 0034; \\ MyPath \\ & \# 0034;. Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa. Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad MEDIAPACKAGEPATH debe establecerse en la nueva ruta de acceso que se va a instalar desde este medio. No se puede usar un origen con una ubicación en el CD-ROM diferente de la especificada en el paquete. Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde los medios de envío.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propiedad MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680490"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="dbff4-106">Propiedad MEDIAPACKAGEPATH</span><span class="sxs-lookup"><span data-stu-id="dbff4-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="dbff4-107">Si el paquete de instalación que se envía con una aplicación no se encuentra en la raíz del CD-ROM que reciben los clientes, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la línea de comandos para la ruta de acceso relativa de la aplicación en el CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="dbff4-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="dbff4-108">Por ejemplo, si la ruta de acceso al paquete en el medio es E: \\ mypath \\My.msi, use MEDIAPACKAGEPATH = " \\ myPath \\ ".</span><span class="sxs-lookup"><span data-stu-id="dbff4-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="dbff4-109">Los administradores pueden crear CD-ROMs desde un punto de instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="dbff4-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="dbff4-110">Si se cambia la ubicación de la raíz de la instalación en los nuevos CD-ROM, la propiedad **MEDIAPACKAGEPATH** debe establecerse en la nueva ruta de acceso que se va a instalar desde este medio.</span><span class="sxs-lookup"><span data-stu-id="dbff4-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="dbff4-111">No se puede usar un origen con una ubicación en el CD-ROM diferente de la especificada en el paquete.</span><span class="sxs-lookup"><span data-stu-id="dbff4-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="dbff4-112">Sin embargo, no es necesario usar esta propiedad al crear un punto de instalación administrativa desde los medios de envío.</span><span class="sxs-lookup"><span data-stu-id="dbff4-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbff4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbff4-113">Requirements</span></span>



| <span data-ttu-id="dbff4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbff4-114">Requirement</span></span> | <span data-ttu-id="dbff4-115">Value</span><span class="sxs-lookup"><span data-stu-id="dbff4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbff4-116">Versión</span><span class="sxs-lookup"><span data-stu-id="dbff4-116">Version</span></span><br/> | <span data-ttu-id="dbff4-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dbff4-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dbff4-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dbff4-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dbff4-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbff4-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dbff4-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dbff4-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbff4-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dbff4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbff4-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbff4-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




