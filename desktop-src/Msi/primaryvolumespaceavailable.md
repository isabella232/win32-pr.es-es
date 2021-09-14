---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceAvailable en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propiedad PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161450"
---
# <a name="primaryvolumespaceavailable-property"></a>Propiedad PrimaryVolumeSpaceAvailable

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceAvailable** en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la [**propiedad PrimaryVolumePath.**](primaryvolumepath.md)

## <a name="remarks"></a>Observaciones

Por ejemplo, si [**PrimaryVolumePath**](primaryvolumepath.md) se establece en "D:" y el volumen D: tiene 446 134 272 bytes libres, **PrimaryVolumeSpaceAvailable** se establece en 871356.

Tenga en cuenta que si este valor se va a mostrar dentro de un [control Text](text-control.md)estático, el bit [FormatSize](formatsize-control-attribute.md) se puede usar para dar formato y etiquetar automáticamente este número en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




