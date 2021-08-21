---
description: El valor de la propiedad COMPADDLOCAL es una lista de GUID de componente de la columna ComponentId de la tabla Component, delimitada por comas, que se van a instalar localmente.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: ComPADDLOCAL, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c442ede6e8affaaddef1dc028a8a6fffc5b780afd536bbc3eaa52e6949df8fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145148"
---
# <a name="compaddlocal-property"></a>ComPADDLOCAL, propiedad

El valor de la propiedad **COMPADDLOCAL** es una lista de GUID de componente de la columna ComponentId de la tabla [Component](component-table.md), delimitada por comas, que se van a instalar localmente. El instalador usa esta lista para determinar qué características se establecen para instalarse localmente, en función de los componentes especificados. Para cada identificador de componente enumerado, el instalador examina todas las características vinculadas a ese componente a través de la tabla [FeatureComponents](featurecomponents-table.md) e instala la característica que requiere la menor cantidad de espacio en disco para instalar. Los componentes enumerados deben estar presentes en la columna Componente de la [tabla](component-table.md) Componente .

## <a name="remarks"></a>Comentarios

Tenga en cuenta que los nombres de componente distinguen mayúsculas de minúsculas. Tenga en cuenta también que si la marca de bits SourceOnly está establecida en la columna Atributos de la tabla [Component](component-table.md) de un componente, el componente se instala para ejecutarse desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**eliminar**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  **COMPADDLOCAL**
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
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

 

 




