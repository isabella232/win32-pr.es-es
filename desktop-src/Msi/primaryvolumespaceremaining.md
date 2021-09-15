---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRemaining en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad PrimaryVolumePath, si se instalaron todas las características seleccionadas actualmente.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473953"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining, propiedad

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRemaining** en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath,**](primaryvolumepath.md) si se instalaron todas las características seleccionadas actualmente. Al igual que [**con la propiedad PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) este número se expresa en unidades de 512 bytes.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que si este valor se va a mostrar dentro de un [control Text](text-control.md)estático, el bit [FormatSize](formatsize-control-attribute.md) se puede usar para dar formato y etiquetar automáticamente este número en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




