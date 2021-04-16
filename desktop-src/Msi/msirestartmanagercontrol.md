---
description: La propiedad MSIRESTARTMANAGERCONTROL especifica si el paquete de Windows Installer usa la funcionalidad del cuadro de diálogo Administrador de reinicio o FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propiedad MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671374"
---
# <a name="msirestartmanagercontrol-property"></a><span data-ttu-id="11ae8-103">Propiedad MSIRESTARTMANAGERCONTROL</span><span class="sxs-lookup"><span data-stu-id="11ae8-103">MSIRESTARTMANAGERCONTROL property</span></span>

<span data-ttu-id="11ae8-104">La propiedad **MSIRESTARTMANAGERCONTROL** especifica si el paquete de Windows Installer usa la funcionalidad del [cuadro de diálogo](filesinuse-dialog.md) administrador de [reinicio](../rstmgr/restart-manager-portal.md) o FilesInUse.</span><span class="sxs-lookup"><span data-stu-id="11ae8-104">The **MSIRESTARTMANAGERCONTROL** Property specifies whether the Windows Installer package uses the [Restart Manager](../rstmgr/restart-manager-portal.md) or [FilesInUse Dialog](filesinuse-dialog.md) functionality.</span></span>

## <a name="value"></a><span data-ttu-id="11ae8-105">Value</span><span class="sxs-lookup"><span data-stu-id="11ae8-105">Value</span></span>



| <span data-ttu-id="11ae8-106">Value</span><span class="sxs-lookup"><span data-stu-id="11ae8-106">Value</span></span>                                                                                        | <span data-ttu-id="11ae8-107">Significado</span><span class="sxs-lookup"><span data-stu-id="11ae8-107">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11ae8-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11ae8-108"><dt>0</dt></span></span> </dl>                 | <span data-ttu-id="11ae8-109">Este es el valor predeterminado si no se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="11ae8-109">This is the default value if the property is not set.</span></span> <span data-ttu-id="11ae8-110">Windows Installer siempre intenta usar el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11ae8-110">Windows Installer always attempts to use the [Restart Manager](../rstmgr/restart-manager-portal.md) on Windows Vista.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="11ae8-111"><dt>Activa</dt></span><span class="sxs-lookup"><span data-stu-id="11ae8-111"><dt>"Disable"</dt></span></span> </dl>         | <span data-ttu-id="11ae8-112">Deshabilita la interacción del paquete con el [Administrador de reinicio](../rstmgr/restart-manager-portal.md).</span><span class="sxs-lookup"><span data-stu-id="11ae8-112">Disables interaction of the package with the [Restart Manager](../rstmgr/restart-manager-portal.md).</span></span> <span data-ttu-id="11ae8-113">Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="11ae8-113">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="11ae8-114"><dt>"DisableShutdown"</dt></span><span class="sxs-lookup"><span data-stu-id="11ae8-114"><dt>"DisableShutdown"</dt></span></span> </dl> | <span data-ttu-id="11ae8-115">Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="11ae8-115">Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="11ae8-116">Esta configuración deshabilita los intentos del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="11ae8-116">This setting disables attempts by the [Restart Manager](../rstmgr/restart-manager-portal.md) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="11ae8-117">El instalador sigue usando el administrador de reinicio para detectar los archivos que usan las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="11ae8-117">The installer still uses the Restart Manager to detect files in use by applications.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="11ae8-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11ae8-118">Remarks</span></span>

<span data-ttu-id="11ae8-119">La propiedad **MSIRESTARTMANAGERCONTROL** se omite si el [Administrador de reinicio](../rstmgr/restart-manager-portal.md) no está disponible o está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="11ae8-119">The **MSIRESTARTMANAGERCONTROL** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

<span data-ttu-id="11ae8-120">El valor de esta propiedad se puede modificar mediante transformaciones o actualizaciones de personalización.</span><span class="sxs-lookup"><span data-stu-id="11ae8-120">The value of this property can be modified using customization transforms or upgrades.</span></span> <span data-ttu-id="11ae8-121">Cambiar el valor de esta propiedad a partir de acciones personalizadas no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="11ae8-121">Changing the value of this property from custom actions has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ae8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11ae8-122">Requirements</span></span>



| <span data-ttu-id="11ae8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="11ae8-123">Requirement</span></span> | <span data-ttu-id="11ae8-124">Value</span><span class="sxs-lookup"><span data-stu-id="11ae8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ae8-125">Versión</span><span class="sxs-lookup"><span data-stu-id="11ae8-125">Version</span></span><br/> | <span data-ttu-id="11ae8-126">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11ae8-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11ae8-127">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11ae8-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11ae8-128">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="11ae8-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11ae8-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11ae8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ae8-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11ae8-130">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="11ae8-131">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="11ae8-131">DisableAutomaticApplicationShutdown</span></span>](disableautomaticapplicationshutdown.md)
</dt> <dt>

[<span data-ttu-id="11ae8-132">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="11ae8-132">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
