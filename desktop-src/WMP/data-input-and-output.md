---
title: Entrada y salida de datos
description: Entrada y salida de datos
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Complementos de Windows Media Player, entrada y salida de datos
- complementos, entrada y salida de datos
- Complementos de procesamiento de señal digital, entrada y salida de datos
- Complementos DSP, entrada y salida de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148813"
---
# <a name="data-input-and-output"></a>Entrada y salida de datos

Windows Media Player proporciona datos de audio o vídeo a los complementos de DSP a través de un búfer de entrada asignado por Windows Media Player. Los complementos DSP devuelven datos procesados a Windows Media Player a través de un búfer de salida que también se asigna a Windows Media Player. Windows Media Player administra el proceso de pasar datos entre sí mismo y el complemento de DSP llamando a métodos implementados por el complemento. Para un complemento que actúa como un objeto multimedia de DirectX (DMO), el proceso funciona de la siguiente manera:

1.  Windows Media Player llama a **IMediaObject::P rocessinput**, pasando un puntero a un objeto **IMEDIABUFFER** al complemento DSP.
2.  El complemento DSP mantiene un recuento de referencias en el objeto de búfer de entrada. El complemento DSP devuelve un **valor HRESULT** correcto o de error adecuado.
3.  Windows Media Player llama a **IMediaObject::P rocessoutput**, pasando un puntero a una matriz de estructuras de búfer de datos de salida de DMO (que contienen búferes de salida) al complemento DSP. **\_ \_ \_**
4.  El complemento de DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado. El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer. A continuación, el complemento DSP devuelve un **valor HRESULT** de éxito o error adecuado.
5.  Windows Media Player representa el contenido en el búfer de salida.

Para un complemento que actúa como una transformación de Media Foundation (MFT), el proceso funciona de la siguiente manera:

-   Windows Media Player llama a **IMFTransform::P rocessinput**, pasando un puntero a un objeto de interfaz **IMFSAMPLE** al complemento DSP.
    1.  El complemento DSP mantiene un recuento de referencias en la interfaz **IMFSample** . El complemento DSP devuelve un **valor HRESULT** correcto o de error adecuado.
    2.  Windows Media Player llama a **IMFTransform::P rocessoutput**, pasando un puntero a una matriz de estructuras de búfer de datos de salida de MFT (que contienen búferes de salida) al complemento DSP. **\_ \_ \_**
    3.  El complemento de DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado. El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer. A continuación, el complemento DSP devuelve un **valor HRESULT** de éxito o error adecuado.
    4.  Windows Media Player representa el contenido en el búfer de salida.

Este proceso se repite continuamente mientras el complemento está habilitado y Windows Media Player tiene contenido para representarlo.

> [!Note]  
> No Escriba código que escriba datos en el búfer de entrada o que lea los datos del búfer de salida. El acceso incorrecto a los búferes de datos puede producir resultados inesperados.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




