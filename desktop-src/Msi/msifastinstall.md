---
description: La propiedad MSIFASTINSTALL se puede usar para reducir el tiempo necesario para instalar un paquete de Windows Installer grande.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propiedad MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653707"
---
# <a name="msifastinstall-property"></a>Propiedad MSIFASTINSTALL

La propiedad **MSIFASTINSTALL** se puede usar para reducir el tiempo necesario para instalar un paquete de Windows Installer grande. La propiedad se puede establecer en la línea de comandos o en la tabla de [propiedades](property-table.md) para configurar las operaciones que el usuario o desarrollador determina que no son esenciales para la instalación.

El valor de la propiedad **MSIFASTINSTALL** puede ser una combinación de los valores siguientes.



| Value | Significado                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valor predeterminado                                                                |
| 1     | No se ha guardado ningún punto de restauración del sistema para esta instalación.                      |
| 2     | Realizar solo los [costos de archivos](file-costing.md) y omitir la comprobación de otros costos. |
| 4     | Reducir la frecuencia de los mensajes de progreso.                                   |



 

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Esta propiedad está disponible a partir de Windows Installer 5,0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



 

 




