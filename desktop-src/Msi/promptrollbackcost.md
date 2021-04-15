---
description: La propiedad PROMPTROLLBACKCOST especifica la acción que realiza el instalador si están habilitadas las funcionalidades de instalación de reversión y no hay suficiente espacio en disco para completar la instalación. Los valores posibles de PROMPTROLLBACKCOST son los siguientes. ValueActionPDisplay un cuadro de diálogo en el que se le pregunta si desea continuar sin una reversión. DDisable revertir y continuar sin preguntar al usuario. FFail con el mensaje de error de espacio insuficiente en disco.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propiedad PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653914"
---
# <a name="promptrollbackcost-property"></a>Propiedad PROMPTROLLBACKCOST

La propiedad **PROMPTROLLBACKCOST** especifica la acción que realiza el instalador si están habilitadas las funcionalidades de [instalación de reversión](rollback-installation.md) y no hay suficiente espacio en disco para completar la instalación.

Los valores posibles de **PROMPTROLLBACKCOST** son los siguientes.



| Value | Acción                                                              |
|-------|---------------------------------------------------------------------|
| P     | Muestra un cuadro de diálogo en el que se le pregunta si desea continuar sin una reversión. |
| D     | Deshabilite la reversión y continúe sin preguntar al usuario.                  |
| F     | Error con el mensaje de error de espacio insuficiente en disco.                       |



 

## <a name="remarks"></a>Observaciones

Cuando la interfaz de usuario se ejecuta en el nivel básico o sin interfaz de usuario, el instalador controla automáticamente toda la lógica de espacio en disco.

Cuando la interfaz de usuario se ejecuta en el nivel completo, se pueden proporcionar opciones adicionales al usuario, como preguntar antes de continuar con una reversión, deshabilitar la reversión o continuar sin reversión cuando el disco está lleno. Depende del desarrollador de paquetes crear la secuencia del cuadro de diálogo para proporcionar las opciones adecuadas al usuario. Los elementos disponibles para ello son las propiedades [EnableRollback ControlEvent,](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) , [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) y **PROMPTROLLBACKCOST** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




