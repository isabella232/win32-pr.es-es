---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en una cadena que representa el número total de bytes requerido por todas las características seleccionadas del volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: PrimaryVolumeSpaceRequired, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161439"
---
# <a name="primaryvolumespacerequired-property"></a>PrimaryVolumeSpaceRequired, propiedad

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRequired** en una cadena que representa el número total de bytes requerido por todas las características seleccionadas en el volumen al que hace referencia la propiedad [**PrimaryVolumePath.**](primaryvolumepath.md) Al igual que [**con la propiedad PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) este número se expresa en unidades de 512 bytes.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que si este valor se va a mostrar dentro de un [control Text](text-control.md)estático, el bit [FormatSize](formatsize-control-attribute.md) se puede usar para dar formato y etiquetar automáticamente este número en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




