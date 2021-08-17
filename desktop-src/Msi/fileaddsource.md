---
description: El valor de la propiedad FILEADDSOURCE denota una lista de claves de archivo delimitadas por comas que se van a instalar para ejecutarse desde el medio de origen.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: Propiedad FILEADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7678c42e683b70fc61e563c57ee234c523078bcdd737bf8f28bc2c05302fbb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636567"
---
# <a name="fileaddsource-property"></a>Propiedad FILEADDSOURCE

El valor de la **propiedad FILEADDSOURCE** denota una lista de claves de archivo delimitadas por comas que se van a instalar para ejecutarse desde el medio de origen. Para cada clave de archivo de la lista, el instalador determina el componente que controla ese archivo y, a continuación, examina todas las características vinculadas a ese componente por la tabla [FeatureComponents](featurecomponents-table.md) e instala la característica que requiere la menor cantidad de espacio en disco. Las claves de archivo de la lista deben estar presentes en la columna Archivo de la [tabla](file-table.md) Archivo.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que los nombres de clave de archivo distinguen mayúsculas de minúsculas. Tenga en cuenta también que si la marca de [](component-table.md) bits LocalOnly está establecida en la columna Atributos de la tabla Componente de un componente, el componente se instala para ejecutarse localmente.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**eliminar**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. **FILEADDSOURCE**
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, MyFeature se establece en run-from-source. Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero MyFeature se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida MyFeature) se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




