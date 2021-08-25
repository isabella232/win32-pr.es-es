---
description: Para deshabilitar la interfaz de usuario insertada para la instalación definida en la tabla MsiEmbeddedUI, establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propiedad MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039955"
---
# <a name="msidisableeeui-property"></a>Propiedad MSIDISABLEEEUI

Para deshabilitar la interfaz de usuario insertada para la instalación definida en la tabla [MsiEmbeddedUI](msiembeddedui-table.md), establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Las versiones anteriores a Windows Installer 4.5 omiten la propiedad MSIDISABLEEEUI.

## <a name="remarks"></a>Comentarios

En una instalación de varios paquetes, un paquete secundario normalmente debe usar la interfaz de usuario del paquete primario y no inicializar su propia interfaz de usuario incrustada. Si la propiedad MSIDISABLEEEUI no está establecida dentro del paquete primario, el paquete secundario usa la interfaz de usuario insertada del paquete primario de forma predeterminada y omite la propiedad MSIDISABLEEEUI dentro del paquete secundario.

La propiedad MSIDISABLEEEUI deshabilita la interfaz de usuario insertada para un único paquete. Puede usar la directiva [MsiDisableEmbeddedUI](msidisableembeddedui.md) para deshabilitar las interfaces de usuario insertadas para todos los paquetes del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.5 en Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




