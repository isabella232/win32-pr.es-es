---
description: El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en una cadena que representa el número total de bytes necesarios para todas las características seleccionadas en el volumen al que hace referencia la propiedad PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propiedad PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654005"
---
# <a name="primaryvolumespacerequired-property"></a>Propiedad PrimaryVolumeSpaceRequired

El instalador establece el valor de la propiedad **PrimaryVolumeSpaceRequired** en una cadena que representa el número total de bytes necesarios para todas las características seleccionadas en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) . Al igual que con la propiedad [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , este número se expresa en unidades de 512 bytes.

## <a name="remarks"></a>Observaciones

Nota: Si este valor se va a mostrar dentro de un [control de texto](text-control.md)estático, se puede usar el bit [formatable](formatsize-control-attribute.md) para dar formato y etiquetar este número automáticamente en unidades de kilobytes o megabytes según corresponda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




