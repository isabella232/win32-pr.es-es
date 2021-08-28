---
description: Al establecer la propiedad ARPNOREMOVE, se deshabilita la funcionalidad Agregar o quitar programas Panel de control que quita el producto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propiedad ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d69e066aeb96861be220a40334d44bf55fe0569e855029d2a19399b56a1c205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105435"
---
# <a name="arpnoremove-property"></a>Propiedad ARPNOREMOVE

Al establecer **la propiedad ARPNOREMOVE,** se deshabilita la funcionalidad Agregar o quitar programas **Panel de control** que quita el producto.  Para Windows 2000, esto deshabilita  el botón Quitar del producto desde agregar o quitar programas **en** **Panel de control**. En sistemas operativos anteriores, esto tiene el efecto de quitar el producto de la lista de productos instalados en agregar o **quitar programas** **en** Panel de control .

Si se **establece la propiedad ARPNOREMOVE,** la [acción RegisterProduct](registerproduct-action.md) escribe el valor "NoRemove" en la clave del Registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalación** \\ **{*clave de producto*}**

Establecer la **propiedad ARPNOREMOVE** impide que el valor UninstallString se escriba en esta clave. El valor UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.

## <a name="remarks"></a>Comentarios

Por ejemplo, esta propiedad se puede establecer durante una transformación de personalización para evitar que los usuarios quiten una personalización de administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 o posterior en Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




