---
description: El valor de la propiedad ADDDEFAULT es una lista de características delimitadas por comas, que se van a instalar en su configuración predeterminada.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propiedad ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653448"
---
# <a name="adddefault-property"></a>Propiedad ADDDEFAULT

El valor de la propiedad **ADDDEFAULT** es una lista de características delimitadas por comas, que se van a instalar en su configuración predeterminada. Las características deben estar presentes en la columna característica de la [tabla de características.](feature-table.md) Para instalar todas las características en sus configuraciones predeterminadas, use ADDDEFAULT = ALL en la línea de comandos.

Una característica enumerada en la propiedad **ADDDEFAULT** se instala en el mismo estado de instalación que si el usuario solicitara una instalación a petición de la característica. El estado viene determinado por los bits establecidos para la característica en la columna Attributes de la [tabla de características](feature-table.md), y los bits que se establecen para los componentes de características en la columna Attributes de la [tabla Component](component-table.md).

## <a name="remarks"></a>Observaciones

Los nombres de las características distinguen mayúsculas de minúsculas.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RETIRAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIA**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo:

-   Si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local **y, a** continuación, se establece en "Run-from-Source".
-   Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la **función** se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = All, todas las características **(incluidas las funciones)** se restablecen a la ejecución desde el origen.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




