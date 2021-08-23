---
title: Creación y optimizaciones de GUID
description: Creación y optimizaciones de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731435"
---
# <a name="guid-creation-and-optimizations"></a>Creación y optimizaciones de GUID

Dado que un CLSID, como un identificador de interfaz (IID), es un GUID, ninguna otra clase, independientemente de quién lo escriba, tiene un CLSID duplicado. Por lo general, los implementadores de servidor obtienen CLID a través [**de la función CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) Se garantiza que esta función genera CLID únicos, por lo que los implementadores de servidores de todo el mundo pueden desarrollar e implementar su software de forma independiente sin miedo a colisiones accidentales con el software escrito por otros usuarios.

El uso de CLSID únicos evita la posibilidad de colisiones de nombres entre clases porque los CLID no están conectados de ninguna manera a los nombres usados en la implementación subyacente. Por ejemplo, dos proveedores diferentes pueden escribir clases denominadas "StackClass", pero cada uno tendría un CLSID único y, por tanto, no se pudo confundir.

COM con frecuencia debe asignar GUID (GUID y CLID) a un conjunto arbitrariamente grande de otros valores. Como desarrollador de aplicaciones, puede ayudar a acelerar estas búsquedas y, por tanto, mejorar el rendimiento del sistema, generando los GUID de la aplicación como un bloque de valores consecutivos.

La manera más eficaz de generar un bloque de GUID consecutivos es ejecutar la utilidad uuidgen mediante los modificadores -n y -x, que genera un bloque de UUID, cada uno de cuyo primer valor DWORD se incrementa en uno.

Por ejemplo, si fuera a escribir

**uuidgen -n5 -x**

la utilidad uuidgen generaría un bloque de UUID similares a los siguientes:

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

Un método para generar y realizar el seguimiento de GUID para todo un proyecto comienza con la generación de un bloque de algunos UUID arbitrariamente grandes, por ejemplo, 500. Por ejemplo, si fuera a escribir

**uuidgen -n500 -x > guids.txt**

la utilidad generaría 500 UUID consecutivos y los escribiría en el archivo de texto especificado. A continuación, puede comprobar este archivo en el árbol de origen, proporcionando un único repositorio para todos los GUID que se usarán en un proyecto. Como los usuarios requieren GUID para sus partes del proyecto, pueden consultar el archivo, tomar el número de GUID que necesiten, marcarlos como tomados y dejar una nota sobre dónde en el código o "especificación" los usan.

Además de mejorar el rendimiento del sistema, la generación de bloques de GUID consecutivos de esta manera tiene las siguientes ventajas:

-   Un archivo central que contiene todos los GUID de una aplicación facilita el seguimiento de qué GUID son para qué y qué personas los usan.
-   Un bloque de GUID consecutivos asociados a una aplicación determinada ayuda a los desarrolladores y evaluadores a reconocer GUID internos durante la depuración y facilita su búsqueda en el registro del sistema porque se almacenan secuencialmente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




