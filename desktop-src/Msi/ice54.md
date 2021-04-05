---
description: ICE54 comprueba los componentes que usan un archivo complementario como su ruta de acceso de clave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910094"
---
# <a name="ice54"></a>ICE54

ICE54 comprueba los componentes que usan un archivo complementario como su ruta de acceso de clave.

El archivo de ruta de acceso de la clave de un componente no debe derivar su versión de un archivo diferente. Esto puede hacer que algunos archivos no se instalen. Vea la [tabla de archivos](file-table.md) para obtener más información acerca de los archivos complementarios.

## <a name="result"></a>Resultado

ICE54 publica una advertencia si algún componente tiene un archivo de ruta de acceso de clave que deriva su versión de otro archivo.

## <a name="example"></a>Ejemplo

ICE54 devuelve la siguiente advertencia para el ejemplo que se muestra.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributo | Rutas |
|------------|-----------|---------|
| Component1 | 0         | Archivo1   |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Versión | Idioma |
|-------|---------|----------|
| Archivo1 | Archivo2   |          |
| Archivo2 | 1.0.0.0 | 3082     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



