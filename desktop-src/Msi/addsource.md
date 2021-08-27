---
description: El valor de la propiedad ADDSOURCE es una lista de características que están delimitadas por comas y que se van a instalar para ejecutarse desde el origen.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: AddSOURCE, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420ca53a96ddeb379a7e021db2c45157861acfb62d066cadfc7a163db7fbc307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078165"
---
# <a name="addsource-property"></a>AddSOURCE, propiedad

El valor de la **propiedad ADDSOURCE** es una lista de características que están delimitadas por comas y que se van a instalar para ejecutarse desde el origen. Las características deben estar presentes en la columna Característica de la [tabla de características](feature-table.md). Para instalar todas las características que se ejecutan desde el origen, use ADDSOURCE=ALL en la línea de comandos. No escriba ADDSOURCE=ALL en la tabla de propiedades [,](property-table.md)ya que esto genera un paquete de ejecución desde el origen que no se puede quitar correctamente.

## <a name="remarks"></a>Comentarios

Los nombres de características distinguen mayúsculas de minúsculas. Si la marca de bits LocalOnly se [](component-table.md) establece en la columna Atributos de la tabla de componentes para un componente de una característica de la lista, ese componente se instala para ejecutarse localmente.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**eliminar**](remove.md)
3.  **ADDSOURCE**
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
-   Si la línea de comandos es: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, primero **MyFeature** se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluido **MyFeature)** se restablecen a run-from-source.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida, o cuando se especifica alguna de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




