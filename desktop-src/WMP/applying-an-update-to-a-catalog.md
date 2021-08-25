---
title: Aplicar una actualización a un catálogo
description: Aplicar una actualización a un catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Reproductor de Windows Media en línea, aplicar actualizaciones a catálogos
- tiendas en línea, aplicación de actualizaciones a catálogos
- tiendas en línea de tipo 1, aplicación de actualizaciones a catálogos
- Reproductor de Windows Media en línea, actualizar catálogos
- tiendas en línea, actualizar catálogos
- tiendas en línea de tipo 1, actualizar catálogos
- Reproductor de Windows Media en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tiendas en línea de tipo 1, actualizaciones del catálogo
- actualizaciones del catálogo
- actualizar catálogos
- aplicación de actualizaciones a catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114b5b341df1101b221a3d8227bf0526bfa32af744f1dca7b0a53ca2d7793c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124035"
---
# <a name="applying-an-update-to-a-catalog"></a>Aplicar una actualización a un catálogo

> [!Note]  
> Normalmente, esto no se hace excepto con fines de diagnóstico, por ejemplo, para ayudar a comprobar que un archivo de diferencia es válido. El catálogo generado de esta manera no está comprimido y no se debe pasar a Reproductor de Windows Media.

 

Se puede crear un nuevo archivo de catálogo mediante la sintaxis siguiente, donde *inputcatalog* es la ubicación del catálogo original y *inputdiff* es la ubicación del archivo de diferencia que se va a aplicar. Los archivos de catálogo deben estar en formato sin comprimir.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Por ejemplo, lo siguiente crea un nuevo catálogo a partir de C: \\ Catalog210 \\ catalog.wmdb y C: \\ Catalog210 \\ catalog.diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Si la compilación se realiza correctamente, catcomp.exe los siguientes archivos de salida.



| Nombre de archivo        | Descripción       |
|------------------|-------------------|
| catalog.wmdb.new | Nuevo archivo de catálogo. |



 

 

 




