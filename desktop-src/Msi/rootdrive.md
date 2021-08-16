---
description: La propiedad ROOTDRIVE especifica la unidad predeterminada para el directorio de destino de la instalación.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propiedad ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ca4a3230dde5086b1383f3016da30d99976cf6560d0be994ecb0aaccc0ba6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625742"
---
# <a name="rootdrive-property"></a>Propiedad ROOTDRIVE

La **propiedad ROOTDRIVE** especifica la unidad predeterminada para el directorio de destino de la instalación. Si la columna Directory de la tabla [Directory](directory-table.md) indica el directorio de destino raíz por un nombre de propiedad que no está definido, el instalador usa el valor de la **propiedad ROOTDRIVE** para resolver la ruta de acceso al directorio de destino.

Si **ROOTDRIVE no** se establece en una línea de comandos o se crea en la [tabla Property](property-table.md), el instalador establece esta propiedad. Durante una [instalación administrativa,](administrative-installation.md) el instalador establece **ROOTDRIVE** en la primera unidad de red conectada en la que encuentra que se puede escribir. Si no se trata de una instalación administrativa o si el instalador no encuentra ninguna unidad de red, el instalador establece **ROOTDRIVE** en la unidad local que se puede escribir para tener el máximo espacio libre.

El valor de esta propiedad debe terminar con \\ ''.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




