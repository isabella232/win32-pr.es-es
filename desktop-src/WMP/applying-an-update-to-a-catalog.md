---
title: Aplicar una actualización a un catálogo
description: Aplicar una actualización a un catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Reproductor de Windows Media en línea, aplicar actualizaciones a los catálogos
- tiendas en línea, aplicación de actualizaciones a catálogos
- tiendas en línea de tipo 1, aplicación de actualizaciones a catálogos
- Reproductor de Windows Media en línea, actualizar catálogos
- tiendas en línea, actualizar catálogos
- tiendas en línea de tipo 1, actualizar catálogos
- Reproductor de Windows Media en línea, actualizaciones de catálogo
- tiendas en línea, actualizaciones de catálogo
- tiendas en línea de tipo 1, actualizaciones de catálogo
- actualizaciones del catálogo
- actualizar catálogos
- aplicación de actualizaciones a catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073287"
---
# <a name="applying-an-update-to-a-catalog"></a>Aplicar una actualización a un catálogo

> [!Note]  
> Normalmente, esto no se hace excepto con fines de diagnóstico, por ejemplo, para ayudar a comprobar que un archivo de diferencia es válido. El catálogo generado de esta manera no está comprimido y no debe pasarse a Reproductor de Windows Media.

 

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



 

 

 




