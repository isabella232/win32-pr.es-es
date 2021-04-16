---
description: El valor de la propiedad ADDLOCAL es una lista de características que están delimitadas por comas y que se van a instalar localmente.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671796"
---
# <a name="addlocal-property"></a>ADDLOCAL (propiedad)

El valor de la propiedad **AddLocal** es una lista de características que están delimitadas por comas y que se van a instalar localmente. Las características deben estar presentes en la columna característica de la [tabla de características](feature-table.md). Para instalar todas las características localmente, utilice ADDLOCAL = ALL en la línea de comandos. No escriba ADDLOCAL = ALL en la [tabla de propiedades](property-table.md), ya que esto genera un paquete instalado localmente que no se puede quitar correctamente.

## <a name="remarks"></a>Observaciones

Los nombres de las características distinguen mayúsculas de minúsculas. Si la marca de bits SourceOnly se establece en la columna atributos de la [tabla componente](component-table.md) para un componente de una característica de la lista, ese componente se instala como ejecutar desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  **ADDLOCAL**
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

Por ejemplo:

-   Si la línea de comandos especifica: ADDLOCAL = ALL, ADDSOURCE = **función**, todas las características se establecen primero en Run-local **y, a** continuación, se establece en "Run-from-Source".
-   Si la línea de comandos es: ADDSOURCE = ALL, ADDLOCAL =**función**, First la **función** se establece en Run-local y, a continuación, cuando se evalúa ADDSOURCE = All, todas las características **(incluidas las funciones)** se restablecen a la ejecución desde el origen.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




