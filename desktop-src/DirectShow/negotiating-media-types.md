---
description: Tipos de medios de negociación
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Tipos de medios de negociación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf3294ed1f7ff31037f0720b7e1644d688f419263962a764de5ea7e40e6b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072929"
---
# <a name="negotiating-media-types"></a>Tipos de medios de negociación

Cuando filter Graph Manager llama al método [**IPin::Conectar,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) tiene varias opciones para especificar un tipo de medio:

-   **Tipo completo:** Si el tipo de medio está totalmente especificado, los pines intentan conectarse con ese tipo. Si no es posible, se produce un error en el intento de conexión.
-   **Tipo de medio parcial:** Un tipo de medio es *parcial si* el tipo principal, subtipo o tipo de formato es GUID \_ NULL. El valor GUID \_ NULL actúa como un "carácter comodín", lo que indica que cualquier valor es aceptable. Los pines negocian un tipo coherente con el tipo parcial.
-   **Sin tipo de medio:** Si filter Graph Manager pasa un puntero **NULL,** los pines pueden aceptar cualquier tipo de medio que sea aceptable para ambos pines.

Si los pines se conectan, la conexión siempre tiene un tipo de medio completo. El propósito del tipo de medio especificado por el Administrador de Graph es limitar los posibles tipos de conexión.

Durante el proceso de negociación, el pin de salida propone un tipo de medio llamando al método [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del pin de entrada. El pin de entrada puede aceptar o rechazar el tipo propuesto. Este proceso se repite hasta que el pin de entrada acepta un tipo o el pin de salida se queda sin tipos y se produce un error en la conexión.

La forma en que un pin de salida selecciona los tipos de medios que se propongan depende de la implementación. En la DirectShow base, el pin de salida llama a [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) en el pin de entrada. Este método devuelve un enumerador que enumera los tipos de medios preferidos del pin de entrada. Si no lo hace, el pin de salida enumera sus propios tipos preferidos.

**Trabajar con tipos de medios**

En cualquier función que reciba un parámetro **AM \_ MEDIA \_ TYPE,** valide siempre los valores de **cbFormat** y **formattype** antes de desreferenciar el **miembro pbFormat.** El código siguiente es incorrecto:


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



 

 



