---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceAvailable en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propiedad PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9336bfa32ebb3bf0c12b7e7fc54ddad2b26cd635c820ca6e8ea2caabe163ceb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580675"
---
# <a name="primaryvolumespaceavailable-property"></a>Propiedad PrimaryVolumeSpaceAvailable

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceAvailable** en una cadena que representa el número total de bytes disponibles, en unidades de 512, en el volumen al que hace referencia la propiedad [**PrimaryVolumePath.**](primaryvolumepath.md)

## <a name="remarks"></a>Comentarios

Por ejemplo, si [**PrimaryVolumePath**](primaryvolumepath.md) se establece en "D:" y el volumen D: tiene 446 134 272 bytes libres, **PrimaryVolumeSpaceAvailable** se establece en 871356.

Tenga en cuenta que si este valor se va a mostrar dentro de un [control Text](text-control.md)estático, el bit [FormatSize](formatsize-control-attribute.md) se puede usar para dar formato y etiquetar automáticamente este número en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




