---
description: Al establecer la propiedad ARPNOMODIFY se deshabilita la funcionalidad Agregar o quitar programas Panel de control que modifica el producto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propiedad ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159085"
---
# <a name="arpnomodify-property"></a>Propiedad ARPNOMODIFY

Al establecer **la propiedad ARPNOMODIFY** se deshabilita la funcionalidad Agregar o quitar programas Panel de control que modifica el producto. Para Windows 2000, esto deshabilita  el botón Modificar  del producto en Agregar o quitar programas **en Panel de control**. En sistemas operativos anteriores, al hacer clic en el botón **Agregar** o quitar programas se desinstala el producto en lugar de entrar en el Asistente para modo de mantenimiento.

Si se establece la propiedad **ARPNOMODIFY,** la acción [RegisterProduct](registerproduct-action.md) escribe el valor "NoModify" en la clave del Registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalación** \\ **{*clave de producto*}**

Si se establece la propiedad **ARPNOMODIFY** y no se establece la propiedad [**ARPNOREMOVE,**](arpnoremove.md) la acción RegisterProduct también escribe el valor UninstallString bajo esta clave. El valor UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.

## <a name="remarks"></a>Observaciones

En Windows 2000, esto deshabilita  el botón Cambiar del  producto en agregar o quitar programas de la **Panel de control**.

Esta propiedad se puede establecer mediante una transformación de personalización para evitar que los usuarios cambien la personalización de un administrador mediante **Agregar o quitar programas.** Esta propiedad solo afecta a **Agregar o quitar programas.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Un ejemplo de transformación de personalización](a-customization-transform-example.md)
</dt> </dl>

 

 




