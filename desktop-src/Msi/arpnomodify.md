---
description: Al establecer la propiedad ARPNOMODIFY, se deshabilita la funcionalidad Agregar o quitar programas Panel de control que modifica el producto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propiedad ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9a097f183c13e1c5b6f8f8b6a521c8a03149df130befaa1221b14b732418a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581815"
---
# <a name="arpnomodify-property"></a>Propiedad ARPNOMODIFY

Al establecer **la propiedad ARPNOMODIFY,** se deshabilita la funcionalidad Agregar o quitar programas Panel de control que modifica el producto. Para Windows 2000, esto deshabilita  el botón Modificar del producto en Agregar o quitar programas **en** **Panel de control**. En sistemas operativos anteriores, al hacer clic en el botón **Agregar** o quitar programas, se desinstala el producto en lugar de entrar en el asistente de modo de mantenimiento.

Si se establece la propiedad **ARPNOMODIFY,** la acción [RegisterProduct](registerproduct-action.md) escribe el valor "NoModify" en la clave del Registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalación** \\ **{*clave de producto*}**

Si se establece la propiedad **ARPNOMODIFY** y no se establece la propiedad [**ARPNOREMOVE,**](arpnoremove.md) la acción RegisterProduct también escribe el valor UninstallString bajo esta clave. El valor UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.

## <a name="remarks"></a>Comentarios

En Windows 2000, esto deshabilita  el botón Cambiar del producto en agregar o quitar **programas** de la **Panel de control**.

Esta propiedad se puede establecer mediante una transformación de personalización para evitar que los usuarios cambien la personalización de un administrador mediante **Agregar o quitar programas.** Esta propiedad solo afecta a **Agregar o quitar programas.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Ejemplo de transformación de personalización](a-customization-transform-example.md)
</dt> </dl>

 

 




