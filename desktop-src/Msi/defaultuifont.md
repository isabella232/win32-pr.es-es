---
description: La propiedad DefaultUIFont establece el estilo de fuente predeterminado que se usa para los controles. Para especificar el valor predeterminado, establezca DefaultUIFont en uno de los estilos predefinidos de la tabla TextStyle en la tabla de propiedades.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propiedad DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654024"
---
# <a name="defaultuifont-property"></a>Propiedad DefaultUIFont

La propiedad **DefaultUIFont** establece el estilo de fuente predeterminado que se usa para los controles. Para especificar el valor predeterminado, establezca **DefaultUIFont** en uno de los estilos predefinidos de la [tabla TextStyle](textstyle-table.md) en la [tabla de propiedades](property-table.md).

## <a name="remarks"></a>Observaciones

La propiedad **DefaultUIFont** de cada paquete de instalación con una interfaz de usuario debe establecerse en la [tabla de propiedades](property-table.md) en uno de los estilos predefinidos enumerados en la [tabla TextStyle](textstyle-table.md). Si no se especifica esta propiedad, el instalador utiliza la fuente del sistema. Esto puede hacer que el instalador muestre de forma incorrecta cadenas de texto cuando la página de códigos del paquete es diferente de la página de códigos de la interfaz de usuario predeterminada del usuario.

El estilo de texto y fuente de un control se puede establecer tal y como se describe en [Agregar controles y texto](adding-controls-and-text.md). Si la cadena de caracteres que se muestra en la columna de texto de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md) no especifica el estilo de fuente, el control utiliza el valor de la propiedad **DefaultUIFont** como estilo de fuente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




