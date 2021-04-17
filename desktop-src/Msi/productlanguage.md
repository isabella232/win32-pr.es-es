---
description: La propiedad ProductLanguage especifica el idioma que debe usar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propiedad ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680660"
---
# <a name="productlanguage-property"></a>Propiedad ProductLanguage

La propiedad **ProductLanguage** especifica el idioma que debe usar el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos. Esta propiedad debe ser un identificador de idioma numérico (LANGID). Si una transformación cambia el idioma de la interfaz de usuario en la base de datos, también debe cambiar el valor de esta propiedad para que refleje el nuevo lenguaje.

Esta propiedad es obligatoria.

## <a name="remarks"></a>Observaciones

El valor de la propiedad **ProductLanguage** debe ser uno de los idiomas enumerados en la propiedad Resumen de la [**plantilla**](template-summary.md) .

Al crear un paquete como independiente del lenguaje, establezca la propiedad **ProductLanguage** en 0 y use la fuente MS Shell Dlg como estilo de texto para todos los diálogos creados. Dado que algunas fuentes no admiten todos los juegos de caracteres, puede asegurarse de que el texto se muestre correctamente en todas las versiones localizadas del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




