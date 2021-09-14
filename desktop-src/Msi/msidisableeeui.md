---
description: Para deshabilitar la interfaz de usuario insertada para la instalación definida en la tabla MsiEmbeddedUI, establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propiedad MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071868"
---
# <a name="msidisableeeui-property"></a>Propiedad MSIDISABLEEEUI

Para deshabilitar la interfaz de usuario insertada para la instalación definida en la tabla [MsiEmbeddedUI](msiembeddedui-table.md), establezca la propiedad MSIDISABLEEEUI en 1 en la línea de comandos.

**[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite. Las versiones anteriores a Windows Installer 4.5 omiten la propiedad MSIDISABLEEEUI.

## <a name="remarks"></a>Observaciones

En una instalación de varios paquetes, un paquete secundario normalmente debe usar la interfaz de usuario del paquete primario y no inicializar su propia interfaz de usuario incrustada. Si la propiedad MSIDISABLEEEUI no se establece dentro del paquete primario, el paquete secundario usa la interfaz de usuario insertada del paquete primario de forma predeterminada e ignora la propiedad MSIDISABLEEEUI dentro del paquete secundario.

La propiedad MSIDISABLEEEUI deshabilita la interfaz de usuario insertada para un único paquete. Puede usar la directiva [MsiDisableEmbeddedUI](msidisableembeddedui.md) para deshabilitar las interfaces de usuario insertadas para todos los paquetes del equipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.5 en Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




