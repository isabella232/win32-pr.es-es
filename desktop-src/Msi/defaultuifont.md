---
description: La propiedad DefaultUIFont establece el estilo de fuente predeterminado que se usa para los controles. Para especificar el valor predeterminado, establezca DefaultUIFont en uno de los estilos predefinidos de la tabla TextStyle de la tabla Property.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propiedad DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bf4c432a0e75c933136cc11e1dd8a55cc6a4cdf2f09c923804132b743e88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289585"
---
# <a name="defaultuifont-property"></a>Propiedad DefaultUIFont

La **propiedad DefaultUIFont** establece el estilo de fuente predeterminado que se usa para los controles. Para especificar el valor predeterminado, **establezca DefaultUIFont** en uno de los estilos predefinidos de la [tabla TextStyle](textstyle-table.md) de la [tabla Property](property-table.md).

## <a name="remarks"></a>Comentarios

La **propiedad DefaultUIFont** de cada paquete de instalación con una interfaz de usuario debe establecerse en la tabla [Property](property-table.md) en uno de los estilos predefinidos enumerados en la [tabla TextStyle](textstyle-table.md). Si no se especifica esta propiedad, el instalador usa la fuente System. Esto puede hacer que el instalador muestre incorrectamente cadenas de texto cuando la página de códigos del paquete es diferente de la página de códigos predeterminada de la interfaz de usuario del usuario.

El texto y el estilo de fuente de un control se pueden establecer como se describe en [Agregar controles y texto.](adding-controls-and-text.md) Si la cadena de caracteres enumerada en la columna Texto de la tabla [Control](control-table.md) o la tabla [BBControl](bbcontrol-table.md) no especifica el estilo de fuente, el control usa el valor de la **propiedad DefaultUIFont** como estilo de fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




