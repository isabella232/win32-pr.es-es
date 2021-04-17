---
description: ICE48 comprueba los directorios que están codificados de forma rígida en las rutas de acceso locales de la tabla de propiedades.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667751"
---
# <a name="ice48"></a>ICE48

ICE48 comprueba los directorios que están codificados de forma rígida en las rutas de acceso locales de la [tabla de propiedades](property-table.md).

No codifique rutas de acceso de directorio a unidades locales porque los equipos difieren en la instalación de la unidad local. Esta práctica puede ser aceptable si se implementa una aplicación en un gran número de equipos en los que las partes relevantes de las unidades son las mismas.

## <a name="result"></a>Resultado

ICE48 envía un mensaje de error si hay un directorio codificado de forma rígida en una ruta de acceso local en la tabla de propiedades.

## <a name="example"></a>Ejemplo

ICE48 notificaría la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Tabla de directorio](directory-table.md) (parcial)



| Directorio | Directorio \_ primario | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad | Value      |
|----------|------------|
| Dir1     | d: \\ origen |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



