---
description: En el siguiente tema se describe cómo realizar una reproducción simple.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Reproducción simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678454"
---
# <a name="simple-playback"></a>Reproducción simple

En el siguiente tema se describe cómo realizar una reproducción simple.

**Para realizar una reproducción simple**

1.  Seleccione el terminal de reproducción de archivos en el nivel de llamada.
2.  Cree el terminal de reproducción en la llamada TAPI.
3.  Establecer propiedades: el nombre de archivo y el tipo de almacenamiento.
4.  Llame al método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el terminal de reproducción de archivos para iniciar la reproducción de secuencias.

En el código de ejemplo siguiente se muestra la reproducción simple.

En primer lugar, use la interfaz [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) para crear el terminal para la grabación. Esto indica a TSP/MSP que realice la reproducción de archivos en esta llamada. El TSP/MSP crea un terminal para que lo use la aplicación y lo devuelve si se ejecuta correctamente.


```C++

```



Obtiene el puntero de la interfaz [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) desde la interfaz de terminal y úselo para establecer el nombre de archivo que se va a reproducir.


```C++
pMediaPlayback->Release();
```



Suponiendo que el archivo contenga una secuencia de audio y que la llamada tenga una secuencia de audio de captura, el contenido de audio del archivo se reproducirá en esa secuencia.

 

 



