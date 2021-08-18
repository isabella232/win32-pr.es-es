---
description: El valor de la propiedad ADDLOCAL es una lista de características que están delimitadas por comas y que se van a instalar localmente.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: AddLOCAL, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82ca86fabd1f90c55c1c3dbf4704a89480a9b23a19f943aca3fd53c1f9065270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822015"
---
# <a name="addlocal-property"></a>AddLOCAL, propiedad

El valor de la **propiedad ADDLOCAL** es una lista de características que están delimitadas por comas y que se van a instalar localmente. Las características deben estar presentes en la columna Característica de la [tabla de características](feature-table.md). Para instalar todas las características localmente, use ADDLOCAL=ALL en la línea de comandos. No escriba ADDLOCAL=ALL en la tabla de propiedades [,](property-table.md)ya que esto genera un paquete instalado localmente que no se puede quitar correctamente.

## <a name="remarks"></a>Comentarios

Los nombres de características distinguen mayúsculas de minúsculas. Si la marca de bits SourceOnly se [](component-table.md) establece en la columna Atributos de la tabla de componentes para un componente de una característica de la lista, ese componente se instala como ejecutado desde el origen.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  **ADDLOCAL**
2.  [**eliminar**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo:

-   Si la línea de comandos especifica: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, todas las características se establecen primero en run-local y, a continuación, **MyFeature** se establece en run-from-source.
-   Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, primero **MyFeature** se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida **MyFeature)** se restablecen a run-from-source.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica alguna de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




