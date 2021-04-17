---
description: Al establecer la propiedad ARPNOMODIFY, se deshabilita la funcionalidad agregar o quitar programas del panel de control que modifica el producto.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propiedad ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653620"
---
# <a name="arpnomodify-property"></a>Propiedad ARPNOMODIFY

Al establecer la propiedad **ARPNOMODIFY** , se deshabilita la funcionalidad agregar o quitar programas del panel de control que modifica el producto. En Windows 2000, Esto deshabilita el botón **modificar** del producto en **Agregar o quitar programas** en el **Panel de control**. En los sistemas operativos anteriores, al hacer clic en el botón **Agregar o quitar programas** , se desinstala el producto en lugar de entrar en el Asistente para el modo de mantenimiento.

Si se establece la propiedad **ARPNOMODIFY** , la [acción RegisterProduct](registerproduct-action.md) escribe el valor "nomodify" en la clave del registro:

**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*clave de producto*}**

Si se establece la propiedad **ARPNOMODIFY** y no se establece la propiedad [**ARPNOREMOVE**](arpnoremove.md) , la acción RegisterProduct también escribe el valor de UninstallString bajo esta clave. El valor de UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.

## <a name="remarks"></a>Observaciones

En Windows 2000, Esto deshabilita el botón **cambiar** del producto en **Agregar o quitar programas** del **Panel de control**.

Esta propiedad se puede establecer mediante una transformación de personalización para evitar que los usuarios cambien la personalización de un administrador a través de **Agregar o quitar programas**. Esta propiedad solo afecta a **Agregar o quitar programas**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Ejemplo de transformación de personalización](a-customization-transform-example.md)
</dt> </dl>

 

 




