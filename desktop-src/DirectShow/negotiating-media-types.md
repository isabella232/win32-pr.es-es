---
description: Negociar tipos de medios
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negociar tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689672"
---
# <a name="negotiating-media-types"></a>Negociar tipos de medios

Cuando el administrador de gráficos de filtro llama al método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , tiene varias opciones para especificar un tipo de medio:

-   **Tipo completo:** Si se especifica el tipo de medio completo, el PIN intenta conectarse con ese tipo. Si no es así, se produce un error en el intento de conexión.
-   **Tipo de medio parcial:** Un tipo de medio es *parcial* si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null. El valor null de GUID \_ actúa como un "carácter comodín", que indica que cualquier valor es aceptable. Los pin negocian un tipo que es coherente con el tipo parcial.
-   **Ningún tipo de medio:** Si Filter Graph Manager pasa un puntero **nulo** , los pin pueden aceptar cualquier tipo de medio que sea aceptable para ambos PIN.

Si los PIN se conectan, la conexión siempre tiene un tipo de medio completo. El propósito del tipo de medio proporcionado por el administrador de gráficos de filtros es limitar los tipos de conexión posibles.

Durante el proceso de negociación, el PIN de salida propone un tipo de medio llamando al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN de entrada. El PIN de entrada puede aceptar o rechazar el tipo propuesto. Este proceso se repite hasta que el PIN de entrada acepta un tipo o el PIN de salida se queda sin tipos y se produce un error en la conexión.

La forma en que un terminal de salida selecciona los tipos de medios que se deben proponer depende de la implementación. En las clases base de DirectShow, el PIN de salida llama a [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) en el PIN de entrada. Este método devuelve un enumerador que enumera los tipos de medios preferidos del PIN de entrada. Si no es así, el PIN de salida enumera sus propios tipos preferidos.

**Trabajar con tipos de medios**

En cualquier función que reciba un parámetro de **\_ \_ tipo de medio am** , valide siempre los valores de **cbFormat** y **formatType** antes de desreferenciar el miembro **pbFormat** . El código siguiente es incorrecto:


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



El código siguiente es correcto:


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



