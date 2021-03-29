---
description: La propiedad ROOTDRIVE especifica la unidad predeterminada para el directorio de destino de la instalación.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propiedad ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679282"
---
# <a name="rootdrive-property"></a>Propiedad ROOTDRIVE

La propiedad **ROOTDRIVE** especifica la unidad predeterminada para el directorio de destino de la instalación. Si la columna de directorio de la [tabla de directorio](directory-table.md) indica el directorio de destino raíz mediante un nombre de propiedad que no está definido, el instalador usa el valor de la propiedad **ROOTDRIVE** para resolver la ruta de acceso al directorio de destino.

Si **ROOTDRIVE** no se establece en una línea de comandos o se crea en la [tabla de propiedades](property-table.md), el instalador establece esta propiedad. Durante una [instalación administrativa](administrative-installation.md) , el instalador establece **ROOTDRIVE** en la primera unidad de red conectada que encuentra en la que se puede escribir. Si no se trata de una instalación administrativa, o si el instalador no puede encontrar ninguna unidad de red, el instalador establece **ROOTDRIVE** en la unidad local que se puede escribir para que tenga más espacio libre.

El valor de esta propiedad debe terminar en ' \\ '.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




