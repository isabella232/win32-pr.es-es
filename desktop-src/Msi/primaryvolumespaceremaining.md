---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRemaining en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad PrimaryVolumePath, si se instalaron todas las características seleccionadas actualmente.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propiedad PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654004"
---
# <a name="primaryvolumespaceremaining-property"></a>Propiedad PrimaryVolumeSpaceRemaining

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRemaining** en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) , si se instalaron todas las características seleccionadas actualmente. Al igual que con la propiedad [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , este número se expresa en unidades de 512 bytes.

## <a name="remarks"></a>Observaciones

Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




