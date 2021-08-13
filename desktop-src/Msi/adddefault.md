---
description: El valor de la propiedad ADDDEFAULT es una lista de características delimitadas por comas, que se instalarán en su configuración predeterminada.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propiedad ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639709"
---
# <a name="adddefault-property"></a>Propiedad ADDDEFAULT

El valor de la **propiedad ADDDEFAULT** es una lista de características delimitadas por comas, que se instalarán en su configuración predeterminada. Las características deben estar presentes en la columna Característica de la [tabla de características.](feature-table.md) Para instalar todas las características en sus configuraciones predeterminadas, use ADDDEFAULT=ALL en la línea de comandos.

Una característica que aparece en la **propiedad ADDDEFAULT** se instala en el mismo estado de instalación que si el usuario solicitara una instalación a petición de la característica. El estado viene determinado por los bits que se establecen para la característica en la columna Atributos de la tabla de características [y](feature-table.md)qué bits se establecen para los componentes de características en la columna Atributos de la tabla [de componentes](component-table.md).

## <a name="remarks"></a>Observaciones

Los nombres de características distinguen mayúsculas de minúsculas.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**eliminar**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo:

-   Si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, **MyFeature** se establece en run-from-source.
-   Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero **MyFeature** se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida **MyFeature)** se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




