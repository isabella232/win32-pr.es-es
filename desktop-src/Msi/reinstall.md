---
description: El valor de la propiedad REINSTALL es una lista de características delimitadas por comas que se van a volver a instalar. Las características enumeradas deben estar presentes en la columna Característica de la tabla Característica. Para volver a instalar todas las características, use REINSTALL=ALL en la línea de comandos.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: REINSTALL, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069674"
---
# <a name="reinstall-property"></a>REINSTALL, propiedad

El valor de la **propiedad REINSTALL** es una lista de características delimitadas por comas que se van a volver a instalar. Las características enumeradas deben estar presentes en la columna Característica de la [tabla](feature-table.md) Característica. Para volver a instalar todas las características, use REINSTALL=ALL en la línea de comandos.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que los nombres de características distinguen mayúsculas de minúsculas.

Si se establece la propiedad **REINSTALL,** también se debe establecer la propiedad [**REINSTALLMODE**](reinstallmode.md) para indicar el tipo de reinstalación que se va a realizar. Si no se establece la propiedad **REINSTALLMODE,** de forma predeterminada se reinstalan todos los archivos que están instalados actualmente, si el archivo instalado actualmente es una versión menor (o no está presente). De forma predeterminada, no se reescribe ninguna entrada del Registro.

Tenga en cuenta que aunque **REINSTALL** esté establecido en ALL, solo se reinstalan las características que ya se instalaron anteriormente. Por lo tanto, si **REINSTALL** está establecido para un producto que aún no está instalado, no se realizará ninguna acción de instalación.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**ELIMINAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  **REINSTALAR**
6.  [**ANUNCIAR**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**FILEADDLOCAL**](fileaddlocal.md)
10. [**FILEADDSOURCE**](fileaddsource.md)
11. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, MyFeature se establece en run-from-source. Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero MyFeature se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida MyFeature) se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




