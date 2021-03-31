---
title: Para enumerar formatos de códecs
description: Para enumerar formatos de códecs
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- secuencias, enumerar formatos de códecs
- códecs, enumeraciones
- secuencias, formatos de códecs
- códecs, formatos
- códecs, interfaz IWMCodecInfo
- IWMCodecInfo, formatos de códecs
- códecs, interfaz IWMCodecInfo3
- IWMCodecInfo3, formatos de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077438"
---
# <a name="to-enumerate-codec-formats"></a>Para enumerar formatos de códecs

Un formato de códec es un objeto de configuración de secuencia que se rellena con datos de un códec. Cada formato de códec contiene una configuración de medios compatible con el códec. La mayoría de los códecs de audio admiten un número finito de formatos, cada uno de los cuales se enumera mediante el códec y se puede tener acceso a ellos mediante los métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). Los códecs de vídeo, por otro lado, solo proporcionan un formato. Esto se debe a que las secuencias de vídeo tienen variables, como el tamaño de fotogramas, que son más flexibles que la configuración de una secuencia de audio. Con un flujo de vídeo, debe rellenar algunos de los valores de configuración de la secuencia. las configuraciones de secuencias de audio solo deben editarse para asignar un nombre, un nombre de conexión y un número de secuencia. Para obtener más información, vea [configuración común para todos los flujos](configuration-common-to-all-streams.md).

Los formatos de códec enumerados dependen de la configuración actual de la enumeración del códec, que se establece mediante [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Actualmente, solo se admiten dos propiedades de códec: g \_ wszNumPasses, que especifica el número de pasos de codificación que realizará el códec y g \_ wszVBREnabled, que especifica si el códec usará codificación de velocidad de bits variable. El número máximo de pasos de codificación admitidos por cualquiera de los códecs es dos, por lo que hay cuatro configuraciones distintas para las que puede recuperar códecs, como se muestra en la tabla siguiente.



|                  | Secuencia de velocidad de bits constante (CBR) | secuencia CBR de 2 pasadas | Secuencia de velocidad de bits variable (VBR) basada en la calidad | Secuencia VBR basada en la velocidad de bits (restringida o sin restricciones) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | false                          | false             | VERDADERO                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Para enumerar los formatos admitidos para un códec, use [**IWMCodecInfo:: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) para buscar el número de códecs admitidos. A continuación, llame a [**IWMCodecInfo:: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) para cada formato. Los índices de formato van desde cero hasta uno menos que el número total de formatos admitidos. Puede recuperar una descripción del formato llamando a [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Cuando se usa **GetCodecFormatDesc**, no es necesario usar **GetCodecFormat**, porque ambos métodos recuperan el objeto de configuración de la secuencia. Los formatos de códec de vídeo no incluyen una descripción. Cada códec de vídeo solo tiene un formato que se utiliza para todos los flujos de ese tipo.

Cuando se recupera un formato de códec, se obtiene la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de un objeto de configuración de secuencia que contiene la configuración de formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de configuración de la secuencia de códecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




