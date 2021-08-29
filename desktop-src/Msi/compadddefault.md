---
description: El valor de la propiedad COMPADDDEFAULT es una lista de GUID de componente de la columna ComponentId de la tabla Component, delimitada por comas, que se instalan en su configuración predeterminada.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: ComPADDDEFAULT, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fdd56c7fd2a74dc9266b7c1648f7e3ce36ccc41c12db2472772c0001b07839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145246"
---
# <a name="compadddefault-property"></a>ComPADDDEFAULT, propiedad

El valor de la **propiedad COMPADDDEFAULT** es una lista de GUID de componente de la columna ComponentId de la tabla [Component](component-table.md), delimitada por comas, que se instalan en su configuración predeterminada. Para cada identificador de componente de la lista, el instalador instala la característica que requiere el menor espacio en disco. Los id. de componente de la lista deben estar presentes en la columna ComponentId de la [tabla Component](component-table.md). Una característica se instala en el mismo estado de instalación que si el usuario hubiera solicitado una instalación a petición de la característica. El estado viene determinado por qué bits se establecen [](feature-table.md)para la característica en la columna Atributos de la tabla Característica y qué bits se establecen para los componentes de la característica en la columna Atributos de la tabla Componente .

## <a name="remarks"></a>Comentarios

Tenga en cuenta que si la marca de bits SourceOnly está establecida en la columna Atributos de la tabla [Component](component-table.md) de un componente, el componente se instala para ejecutarse desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**eliminar**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  **COMPADDDEFAULT**
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, MyFeature se establece en run-from-source. Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero MyFeature se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida MyFeature) se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




