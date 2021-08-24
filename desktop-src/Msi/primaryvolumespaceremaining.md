---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRemaining en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad PrimaryVolumePath, si se instalaron todas las características seleccionadas actualmente.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580495"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining, propiedad

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRemaining** en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath,**](primaryvolumepath.md) si se instalaron todas las características seleccionadas actualmente. Al igual que [**con la propiedad PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) este número se expresa en unidades de 512 bytes.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que si este valor se va a mostrar dentro de un [control Text](text-control.md)estático, el bit [FormatSize](formatsize-control-attribute.md) se puede usar para dar formato y etiquetar automáticamente este número en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




