---
title: Aplicar una actualización a un catálogo
description: Aplicar una actualización a un catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player tiendas en línea, aplicar actualizaciones a catálogos
- tiendas en línea, aplicar actualizaciones a catálogos
- tipo 1 almacenes en línea, aplicar actualizaciones a catálogos
- Windows Media Player tiendas en línea, actualizar catálogos
- tiendas en línea, actualizar catálogos
- tipo 1 almacenes en línea, actualizar catálogos
- Windows Media Player tiendas en línea, actualizaciones del catálogo
- tiendas en línea, actualizaciones del catálogo
- tipo 1 almacenes en línea, actualizaciones del catálogo
- actualizaciones del catálogo
- actualizar catálogos
- aplicar actualizaciones a catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695476"
---
# <a name="applying-an-update-to-a-catalog"></a>Aplicar una actualización a un catálogo

> [!Note]  
> Normalmente, esto no se hace salvo con fines de diagnóstico, por ejemplo, para ayudar a comprobar que un archivo de diferencias es válido. El catálogo generado de esta manera no está en formato comprimido y no se debe pasar a Windows Media Player.

 

Se puede crear un nuevo archivo de catálogo mediante la sintaxis siguiente, donde *inputcatalog* es la ubicación del catálogo original y *inputdiff* es la ubicación del archivo de diferencia que se va a aplicar. Los archivos de catálogo deben estar en un formato sin comprimir.


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



Por ejemplo, lo siguiente crea un nuevo catálogo a partir de C: \\ Catalog210 \\ Catalog. Wmdb y C: \\ Catalog210 \\ Catalog. diff.


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



Si la compilación se realiza correctamente, catcomp.exe crea los siguientes archivos de salida.



| Nombre de archivo        | Descripción       |
|------------------|-------------------|
| Catalog. wmdb. New | Nuevo archivo de catálogo. |



 

 

 




