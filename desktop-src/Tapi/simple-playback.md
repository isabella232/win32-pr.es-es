---
description: En el tema siguiente se describe cómo realizar una reproducción sencilla.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Reproducción simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51724b92fea0a46850609e96de85231a9f1df1f7e538f6def4df07442ef19ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862237"
---
# <a name="simple-playback"></a>Reproducción simple

En el tema siguiente se describe cómo realizar una reproducción sencilla.

**Para realizar una reproducción sencilla**

1.  Seleccione el Terminal de reproducción de archivos en el nivel de llamada.
2.  Cree el terminal de reproducción en la llamada TAPI.
3.  Establecer propiedades: nombre de archivo y tipo de almacenamiento.
4.  Llame al [**método Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) en el Terminal de reproducción de archivos para iniciar la reproducción de secuencias.

En el código de ejemplo siguiente se muestra una reproducción sencilla.

En primer lugar, use [**la interfaz ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) para crear el terminal para la grabación. Esto indica al TSP/MSP que realice la reproducción de archivos en esta llamada. El TSP/MSP crea un terminal para que la aplicación lo use y lo devuelve si se ejecuta correctamente.


```C++

```



Obtenga el [**puntero de la interfaz ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) de la interfaz de terminal y úselo para establecer el nombre de archivo que se va a reproducir.


```C++
pMediaPlayback->Release();
```



Suponiendo que el archivo contiene una secuencia de audio y la llamada tiene una secuencia de audio de captura, el contenido de audio del archivo se reproducirá en esa secuencia.

 

 



