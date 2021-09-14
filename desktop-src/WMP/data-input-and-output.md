---
title: Entrada y salida de datos
description: Entrada y salida de datos
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Reproductor de Windows Media complementos, entrada de datos y salida
- complementos, entrada y salida de datos
- complementos de procesamiento de señal digital, entrada de datos y salida
- Complementos de DSP, entrada y salida de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242547"
---
# <a name="data-input-and-output"></a>Entrada y salida de datos

Reproductor de Windows Media datos de audio o vídeo a los complementos DSP a través de un búfer de entrada asignado por Reproductor de Windows Media. Los complementos de DSP devuelven datos procesados para Reproductor de Windows Media a través de un búfer de salida que también se asigna mediante Reproductor de Windows Media. Reproductor de Windows Media el proceso de pasar datos entre sí y el complemento DSP mediante una llamada a los métodos implementados por el complemento. Para un complemento que actúa como un objeto multimedia DirectX (DMO), el proceso funciona de la siguiente manera:

1.  Reproductor de Windows Media llama a **IMediaObject::P rocessInput** y pasa un puntero a un objeto **IMediaBuffer** al complemento DSP.
2.  El complemento DSP mantiene un recuento de referencias en el objeto de búfer de entrada. El complemento DSP devuelve un HRESULT correcto o **con error adecuado.**
3.  Reproductor de Windows Media llama a **IMediaObject::P rocessOutput** y pasa un puntero DMO una matriz de estructuras **OUTPUT DATA \_ \_ \_ BUFFER** (que contienen búferes de salida) al complemento DSP.
4.  El complemento DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado. El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer. A continuación, el complemento DSP devuelve un valor HRESULT correcto o **de error adecuado.**
5.  Reproductor de Windows Media representa el contenido en el búfer de salida.

En el caso de un complemento que actúa como Media Foundation transform (MFT), el proceso funciona de la siguiente manera:

-   Reproductor de Windows Media llama a **IMFTransform::P rocessInput** y pasa un puntero a un objeto de interfaz **DE PRUEBA AL** COMPLEMENTO DSP.
    1.  El complemento DSP mantiene un recuento de referencias en la **interfaz DESEJEMPLOEjemplo.** El complemento DSP devuelve un HRESULT correcto o **con error adecuado.**
    2.  Reproductor de Windows Media llama a **IMFTransform::P rocessOutput** y pasa un puntero a una matriz de estructuras DE BÚFER DE DATOS DE SALIDA de **MFT \_ \_ \_** (que contienen búferes de salida) al complemento DSP.
    3.  El complemento DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado. El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer. A continuación, el complemento DSP devuelve un valor HRESULT correcto o **de error adecuado.**
    4.  Reproductor de Windows Media representa el contenido en el búfer de salida.

Este proceso se repite continuamente mientras el complemento está habilitado y Reproductor de Windows Media contenido para representar.

> [!Note]  
> No escriba código que escriba datos en el búfer de entrada ni lea datos del búfer de salida. El acceso incorrecto a los búferes de datos puede producir resultados inesperados.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




