---
description: La propiedad Preselected indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección. Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propiedad preseleccionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161454"
---
# <a name="preselected-property"></a>Propiedad preseleccionada

La **propiedad Preselected** indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección.

Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor. Por ejemplo, la propiedad se puede usar para suprimir los diálogos que implican selecciones de características durante la reanudación de una instalación suspendida.

El instalador establece la propiedad **Preselected** en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las siguientes propiedades en la línea de comandos. Si la **propiedad Preselected** se ha establecido en 1, el instalador no usa la tabla [Condition](condition-table.md) para evaluar la selección de características. Las características se instalan en función de las siguientes propiedades. El instalador siempre evalúa estas propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**ELIMINAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIAR**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




