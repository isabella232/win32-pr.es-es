---
title: Creación y optimización de GUID
description: Creación y optimización de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419099"
---
# <a name="guid-creation-and-optimizations"></a>Creación y optimización de GUID

Dado que un CLSID, como un identificador de interfaz (IID), es un GUID, ninguna otra clase, independientemente de quién lo escribe, tiene un CLSID duplicado. Los implementadores de servidor generalmente obtienen CLSID a través de la función [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) . Se garantiza que esta función genera CLSID únicos, de modo que los implementadores del servidor en todo el mundo pueden desarrollar e implementar de forma independiente su software sin miedo a colisiones accidentales con software escrito por otros usuarios.

El uso de CLSID únicos evita la posibilidad de que se produzcan conflictos de nombres entre las clases, ya que los CLSID no se conectan a los nombres utilizados en la implementación subyacente. Por ejemplo, dos proveedores diferentes pueden escribir clases denominadas "StackClass", pero cada una tendría un CLSID único y, por lo tanto, no se pudo confundir.

A menudo, COM debe asignar GUID (IID y CLSID) a un conjunto de otros valores arbitrariamente grande. Como desarrollador de aplicaciones, puede ayudar a acelerar dichas búsquedas y, de este modo, mejorar el rendimiento del sistema mediante la generación de los GUID de la aplicación como un bloque de valores consecutivos.

La manera más eficaz de generar un bloque de GUID consecutivos es ejecutar la utilidad uuidgen mediante los modificadores-n y-x, que genera un bloque de UUID, cada uno de los cuales se incrementa en uno.

Por ejemplo, si fuera a escribir

**uuidgen-N5-x**

la utilidad uuidgen generaría un bloque de UUID similar al siguiente:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Un método para generar y realizar el seguimiento de los GUID para un proyecto completo comienza con la generación de un bloque de un número de UUID arbitrariamente grande, por ejemplo, 500. Por ejemplo, si fuera a escribir

**uuidgen-N500-x > guids.txt**

la utilidad generará 500 UUID consecutivos y los escribirá en el archivo de texto especificado. A continuación, podría comprobar este archivo en el árbol de origen, lo que proporciona un único repositorio para todos los GUID que se usarán en un proyecto. A medida que los usuarios requieren GUID para sus partes del proyecto, pueden desproteger el archivo, no usar muchos de los GUID que necesitan y marcarlos como tomados y dejar una nota sobre la ubicación en el código o "especificación" que los están usando.

Además de mejorar el rendimiento del sistema, la generación de bloques de GUID consecutivos de esta manera presenta las siguientes ventajas:

-   Un archivo central que contiene todos los GUID de una aplicación facilita el seguimiento de qué GUID son para qué y qué usuarios los están usando.
-   Un bloque de GUID consecutivos asociado a una aplicación concreta ayuda a los desarrolladores y evaluadores a reconocer GUID internos durante la depuración y facilita su búsqueda en el registro del sistema porque se almacenan secuencialmente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




