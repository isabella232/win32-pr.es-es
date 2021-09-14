---
description: La propiedad PROMPTROLLBACKCOST especifica la acción que realiza el instalador si las funcionalidades de instalación de reversión están habilitadas y no hay suficiente espacio en disco para completar la instalación. Los valores posibles de PROMPTROLLBACKCOST son los siguientes. ValueActionPDisplay un cuadro de diálogo que pregunta si se debe continuar sin una reversión. Reversión de DDisable y continuar sin preguntar al usuario. FFail con el mensaje de error de espacio fuera del disco.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propiedad PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069751"
---
# <a name="promptrollbackcost-property"></a>Propiedad PROMPTROLLBACKCOST

La **propiedad PROMPTROLLBACKCOST** especifica la acción [](rollback-installation.md) que realiza el instalador si las funcionalidades de instalación de reversión están habilitadas y no hay suficiente espacio en disco para completar la instalación.

Los valores posibles **de PROMPTROLLBACKCOST** son los siguientes.



| Value | Acción                                                              |
|-------|---------------------------------------------------------------------|
| P     | Muestra un cuadro de diálogo que pregunta si se debe continuar sin una reversión. |
| D     | Deshabilite la reversión y continúe sin preguntar al usuario.                  |
| F     | Se produce un error con el mensaje de error de espacio fuera del disco.                       |



 

## <a name="remarks"></a>Observaciones

Cuando la interfaz de usuario se ejecuta en el nivel Básico o sin interfaz de usuario, el instalador controla automáticamente toda la lógica de espacio fuera del disco.

Cuando la interfaz de usuario se ejecuta en el nivel Full, se pueden proporcionar opciones adicionales al usuario, como preguntar antes de continuar con una reversión, deshabilitar la reversión o continuar sin reversión cuando el disco está lleno. Es el desarrollador del paquete el que debe crear la secuencia del cuadro de diálogo para proporcionar las opciones adecuadas al usuario. Los elementos disponibles para ello son la propiedad [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace,**](outofdiskspace.md) [**outOfNoRbDiskSpace**](outofnorbdiskspace.md) y **la propiedad PROMPTROLLBACKCOST.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




