---
description: El valor de la propiedad COMPADDSOURCE es una lista de GUID de componente de la columna ComponentId de la tabla Component, delimitada por comas, que se van a instalar para ejecutarse desde el medio de origen.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: ComPADDSOURCE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158857"
---
# <a name="compaddsource-property"></a>ComPADDSOURCE, propiedad

El valor de la propiedad **COMPADDSOURCE** es una lista de GUID de componente de la columna ComponentId de la tabla [Component,](component-table.md) delimitada por comas, que se van a instalar para ejecutarse desde el medio de origen. El instalador usa este valor para determinar qué características están configuradas para instalarse para ejecutarse desde el origen, en función de los componentes especificados. Para cada identificador de componente enumerado, el instalador examina todas las características vinculadas (a través de la tabla [FeatureComponents)](featurecomponents-table.md) a ese componente e instala la característica que requiere la menor cantidad de espacio en disco para instalar. Los componentes enumerados deben estar presentes en la columna Componente de la [tabla](component-table.md) Componente .

## <a name="remarks"></a>Observaciones

Tenga en cuenta que los nombres de componente distinguen mayúsculas de minúsculas. Tenga en cuenta también que si la marca de bits LocalOnly está establecida en la columna Atributos de la tabla [Component](component-table.md) de un componente, el componente se instala para ejecutarse localmente.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**ELIMINAR**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIAR**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, MyFeature se establece en run-from-source. Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero MyFeature se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida MyFeature) se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




