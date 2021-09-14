---
description: Configuración de códecs MFT
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configuración de códecs MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361162"
---
# <a name="configuring-codec-mfts"></a>Configuración de códecs MFT

En este tema se describe el proceso de configuración de los códecs MFT. Cada códec tiene procedimientos específicos, pero la información común a todos se describe aquí.

## <a name="configuring-mft-inputs-and-outputs"></a>Configuración de entradas y salidas de MFT

Cada MFT admite tipos de entrada y salida específicos. Puede recuperar los tipos de entrada admitidos llamando repetidamente [**a IMFTransform::GetInputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)incrementando el índice de tipo con cada llamada. Cuando encuentre un tipo adecuado, establezca el tipo de entrada mediante una llamada [**a IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype). A continuación, puede repetir el proceso para el tipo de salida mediante las llamadas [**ASETransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) y [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Debe consultar o establecer los tipos de salida disponibles solo después de establecer el tipo de entrada.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Configuración de las MTA de códec para la codificación

Todos los códecs Windows audio multimedia y vídeo admiten una variedad de características de codificación. Por lo general, estas características se configuran estableciendo propiedades en MFT mediante los métodos de la **interfaz IPropertyStore.** Algunas propiedades se configuran mediante interfaces de códec especializadas. Estas interfaces se enumeran para cada códec en la sección [Objetos de códec](codecobjects.md).

El orden general de las operaciones para configurar un MFT de codificación es el siguiente:

1.  Configure las características de códec según sea necesario mediante los métodos **de IPropertyStore**.
2.  Use las interfaces MFT del códec para configurar características adicionales, si es necesario.
3.  Configure los tipos de entrada y salida. El orden en que se deben configurar los tipos varía en función de los códecs individuales. Para obtener más información, [vea Trabajar con audio](workingwithaudio.md) y Trabajar con [vídeo.](workingwithvideo.md)

## <a name="configuring-the-codec-mfts-for-decoding"></a>Configuración de las MTA de códecs para lacoding

La descodificación es más sencilla que la codificación, ya que se admiten menos características de descodificador.

El orden general de las operaciones para configurar una MFT decoding es el siguiente:

1.  Configure las características del descodificador según sea necesario mediante los métodos **de IPropertyStore**.
2.  Establezca el tipo de entrada en el tipo utilizado para la salida del codificador.
3.  Configure el tipo de salida. Los tipos de salida admitidos son diferentes para las distintas entradas.

> [!Note]  
> Es importante usar el mismo tipo de medio para la entrada del descodificador que se usó para la salida del codificador. Esto se debe a que Windows códecs de audio y vídeo multimedia usan formatos multimedia con datos adicionales. Sin los datos de formato extendido, no se puede descodificar el contenido comprimido.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códecs MFT](workingwithcodecmfts.md)
</dt> </dl>

 

 



