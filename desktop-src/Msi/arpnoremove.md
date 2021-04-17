---
description: Al establecer la propiedad ARPNOREMOVE, se deshabilita la funcionalidad agregar o quitar programas del panel de control que quita el producto.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propiedad ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670833"
---
# <a name="arpnoremove-property"></a>Propiedad ARPNOREMOVE

Al establecer la propiedad **ARPNOREMOVE** , se deshabilita la funcionalidad **Agregar o quitar programas** del **Panel de control** que quita el producto. En Windows 2000, Esto deshabilita el botón **quitar** del producto en **Agregar o quitar programas** en el **Panel de control**. En el caso de los sistemas operativos anteriores, esto tiene el efecto de quitar el producto de la lista de productos instalados en **Agregar o quitar programas** en el **Panel de control**.

Si se establece la propiedad **ARPNOREMOVE** , la [acción RegisterProduct](registerproduct-action.md) escribe el valor "noremove" en la clave del registro:

**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ **{*clave de producto*}**

El establecimiento de la propiedad **ARPNOREMOVE** evita que el valor de UninstallString se escriba en esta clave. El valor de UnistallString es una línea de comandos para quitar el producto, en lugar de volver a configurar el producto.

## <a name="remarks"></a>Observaciones

Por ejemplo, esta propiedad se puede establecer durante una transformación de personalización para impedir que los usuarios quiten una personalización de administrador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 o posterior en Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




