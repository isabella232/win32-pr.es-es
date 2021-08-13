---
description: La propiedad MSIFASTINSTALL se puede usar para reducir el tiempo necesario para instalar un paquete Windows Installer.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propiedad MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28c731d34e769f0612acc12586349247231bce663036d3577f41df6a7256f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628512"
---
# <a name="msifastinstall-property"></a>Propiedad MSIFASTINSTALL

La **propiedad MSIFASTINSTALL** se puede usar para reducir el tiempo necesario para instalar un paquete Windows Installer. La propiedad se puede establecer en la línea de comandos o en la tabla [Property](property-table.md) para configurar las operaciones que el usuario o desarrollador determina que no son esenciales para la instalación.

El valor de la **propiedad MSIFASTINSTALL** puede ser una combinación de los valores siguientes.



| Value | Significado                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valor predeterminado                                                                |
| 1     | No se guarda ningún punto de restauración del sistema para esta instalación.                      |
| 2     | Realice solo los [costos de archivo](file-costing.md) y omita la comprobación de otros costos. |
| 4     | Reduzca la frecuencia de los mensajes de progreso.                                   |



 

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta propiedad está disponible a partir de Windows Installer 5.0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



 

 




