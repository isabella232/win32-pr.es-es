---
description: La propiedad ProductLanguage especifica el idioma que el instalador debe usar para las cadenas de la interfaz de usuario que no se han escrito en la base de datos.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Propiedad ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069765"
---
# <a name="productlanguage-property"></a>Propiedad ProductLanguage

La **propiedad ProductLanguage** especifica el idioma que el instalador debe usar para las cadenas de la interfaz de usuario que no se han escrito en la base de datos. Esta propiedad debe ser un identificador de idioma numérico (LANGID). Si una transformación cambia el idioma de la interfaz de usuario en la base de datos, también debe cambiar el valor de esta propiedad para reflejar el nuevo idioma.

Esta propiedad es REQUIRED.

## <a name="remarks"></a>Observaciones

El valor de la **propiedad ProductLanguage** debe ser uno de los idiomas enumerados en la [**propiedad Resumen de**](template-summary.md) plantilla.

Al crear un paquete como sin idioma, establezca la propiedad **ProductLanguage** en 0 y use la fuente Dlg de MS Shell como estilo de texto para todos los diálogos escritos. Dado que algunas fuentes no admiten todos los juegos de caracteres, con esta fuente puede asegurarse de que el texto se muestra correctamente en todas las versiones localizadas del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




