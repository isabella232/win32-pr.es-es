---
description: El valor de la propiedad COMPADDDEFAULT es una lista de GUID de componentes de la columna ComponentId de la tabla de componentes, delimitado por comas, que se instalan en su configuración predeterminada.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Propiedad COMPADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653531"
---
# <a name="compadddefault-property"></a>Propiedad COMPADDDEFAULT

El valor de la propiedad **COMPADDDEFAULT** es una lista de GUID de componentes de la columna ComponentID de la [tabla de componentes](component-table.md), delimitado por comas, que se instalan en su configuración predeterminada. Para cada identificador de componente de la lista, el instalador instala la característica que requiere el menor espacio en disco. Los identificadores de componente de la lista deben estar presentes en la columna ComponentId de la [tabla de componentes](component-table.md). Una característica se instala en el mismo estado de instalación que si el usuario hubiera solicitado una instalación a petición de la característica. El estado se determina por qué bits se establecen para la característica en la columna Attributes de la [tabla de características](feature-table.md)y qué bits se establecen para los componentes de la característica en la columna Attributes de la tabla Component.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que si la marca de bits SourceOnly se establece en la columna Attributes de la tabla de [componentes](component-table.md) para un componente, el componente se instala para ejecutarse desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RETIRAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIA**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  **COMPADDDEFAULT**
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen. Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen a la ejecución desde el origen.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




