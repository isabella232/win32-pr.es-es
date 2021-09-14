---
description: La propiedad MSIFASTINSTALL se puede usar para reducir el tiempo necesario para instalar un paquete Windows Installer.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propiedad MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071857"
---
# <a name="msifastinstall-property"></a>Propiedad MSIFASTINSTALL

La **propiedad MSIFASTINSTALL** se puede usar para reducir el tiempo necesario para instalar un paquete Windows Installer. La propiedad se puede establecer en la línea de comandos o en la tabla [Property](property-table.md) para configurar las operaciones que el usuario o el desarrollador determine que no son esenciales para la instalación.

El valor de la **propiedad MSIFASTINSTALL** puede ser una combinación de los valores siguientes.



| Value | Significado                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valor predeterminado                                                                |
| 1     | No se guarda ningún punto de restauración del sistema para esta instalación.                      |
| 2     | Realice solo [el costo de archivos](file-costing.md) y omita la comprobación de otros costos. |
| 4     | Reduzca la frecuencia de los mensajes de progreso.                                   |



 

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Esta propiedad está disponible a partir de Windows Installer 5.0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



 

 




