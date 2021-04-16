---
description: El valor de la propiedad COMPADDLOCAL es una lista de GUID de componentes de la columna ComponentId de la tabla de componentes, delimitado por comas, que se van a instalar localmente.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: Propiedad COMPADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e403459f0355c28d66da00170b9c649084afbb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671792"
---
# <a name="compaddlocal-property"></a>Propiedad COMPADDLOCAL

El valor de la propiedad **COMPADDLOCAL** es una lista de GUID de componentes de la columna ComponentID de la [tabla de componentes](component-table.md), delimitado por comas, que se van a instalar localmente. El instalador usa esta lista para determinar qué características están configuradas para instalarse localmente, en función de los componentes especificados. Para cada identificador de componente de la lista, el instalador examina todas las características vinculadas a ese componente a través de la tabla [FeatureComponents](featurecomponents-table.md) e instala la característica que requiere la menor cantidad de espacio en disco que se va a instalar. Los componentes enumerados deben estar presentes en la columna componente de la tabla [componente](component-table.md) .

## <a name="remarks"></a>Observaciones

Tenga en cuenta que los nombres de los componentes distinguen mayúsculas de minúsculas. Tenga en cuenta también que si la marca de bits SourceOnly se establece en la columna atributos de la tabla [componente](component-table.md) para un componente, el componente se instala para ejecutarse desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**RETIRAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIA**](advertise.md)
7.  **COMPADDLOCAL**
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
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

 

 




