---
description: La propiedad preseleccionada indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección. Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propiedad preseleccionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653861"
---
# <a name="preselected-property"></a>Propiedad preseleccionada

La propiedad **preseleccionada** indica que las características ya se han seleccionado y que no es necesario mostrar el cuadro de diálogo de selección.

Las expresiones condicionales que dependen de si las características ya están instaladas usan este valor. Por ejemplo, la propiedad se puede utilizar para suprimir los cuadros de diálogo que impliquen selecciones de características durante la reanudación de una instalación suspendida.

El instalador establece la propiedad **preseleccionada** en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las siguientes propiedades en la línea de comandos. Si la propiedad **preseleccionada** se ha establecido en 1, el instalador no utiliza la [tabla de condiciones](condition-table.md) para evaluar la selección de características. Las características se instalan en función de las siguientes propiedades. El instalador siempre evalúa estas propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RETIRAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIA**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




