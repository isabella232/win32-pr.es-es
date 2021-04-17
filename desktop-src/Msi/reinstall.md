---
description: El valor de la propiedad REINSTALL es una lista de características delimitadas por comas que se van a volver a instalar. Las características enumeradas deben estar presentes en la columna característica de la tabla de características. Para reinstalar todas las características, utilice REINSTALL = ALL en la línea de comandos.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: REINSTALL (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653660"
---
# <a name="reinstall-property"></a>REINSTALL (propiedad)

El valor de la propiedad **REINSTALL** es una lista de características delimitadas por comas que se van a volver a instalar. Las características enumeradas deben estar presentes en la columna característica de la tabla de [características](feature-table.md) . Para reinstalar todas las características, utilice REINSTALL = ALL en la línea de comandos.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que los nombres de las características distinguen mayúsculas de minúsculas.

Si se establece la propiedad **REINSTALL** , también se debe establecer la propiedad [**REINSTALLMODE**](reinstallmode.md) para indicar el tipo de reinstalación que se va a realizar. Si no se establece la propiedad **REINSTALLMODE** , de forma predeterminada se reinstalan todos los archivos instalados actualmente, si el archivo instalado actualmente es una versión anterior (o no está presente). De forma predeterminada, no se reescriben entradas del registro.

Tenga en cuenta que incluso si **reinstalar** está establecido en todos, solo se reinstalan las características que ya se instalaron anteriormente. Por lo tanto, si la **reinstalación** está establecida para un producto que todavía está instalado, no se realizará ninguna acción de instalación.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RETIRAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  **REINSTALAR**
6.  [**ANUNCIA**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**FILEADDLOCAL**](fileaddlocal.md)
10. [**FILEADDSOURCE**](fileaddsource.md)
11. [**FILEADDDEFAULT**](fileadddefault.md)

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

 

 




