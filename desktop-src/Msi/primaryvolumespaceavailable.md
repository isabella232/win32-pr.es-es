---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceAvailable en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propiedad PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653601"
---
# <a name="primaryvolumespaceavailable-property"></a>Propiedad PrimaryVolumeSpaceAvailable

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceAvailable** en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) .

## <a name="remarks"></a>Observaciones

Por ejemplo, si [**PrimaryVolumePath**](primaryvolumepath.md) se establece en "D:", y el volumen D: tiene 446.134.272 bytes libres, **PrimaryVolumeSpaceAvailable** se establece en 871356.

Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




