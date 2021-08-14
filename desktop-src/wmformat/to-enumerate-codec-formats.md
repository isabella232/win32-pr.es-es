---
title: Para enumerar formatos de códec
description: Para enumerar formatos de códec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- secuencias, enumeración de formatos de códec
- codecs,enumerations
- streams,codec formats
- códecs, formatos
- codecs,IWMCodecInfo (interfaz)
- IWMCodecInfo, formatos de códec
- codecs,IWMCodecInfo3 (interfaz)
- IWMCodecInfo3, formatos de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221b675c5aa3b5602bcfda96b22233f77d4ba92199f29f36885a4053700dfd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196521"
---
# <a name="to-enumerate-codec-formats"></a>Para enumerar formatos de códec

Un formato de códec es un objeto de configuración de secuencia rellenado con datos de un códec. Cada formato de códec contiene una configuración de medios compatible con el códec. La mayoría de los códecs de audio admiten un número finito de formatos, cada uno de los cuales se enumera mediante el códec y se puede acceder a ellos mediante los métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). Por otro lado, los códecs de vídeo solo proporcionan un formato único. Esto se debe a que las secuencias de vídeo tienen variables, como el tamaño del fotograma, que son más flexibles que la configuración de una secuencia de audio. Con una secuencia de vídeo, debe rellenar algunos de los valores de configuración de la secuencia. Las configuraciones de secuencias de audio solo se deben editar para asignar un nombre, un nombre de conexión y un número de secuencia. Para obtener más información, vea [Configuración común a todos Secuencias](configuration-common-to-all-streams.md).

Los formatos de códec enumerados dependen de la configuración de enumeración de códecs actual, que se establece mediante [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Actualmente, solo se admiten dos propiedades de códec: g wszNumPasses, que especifica el número de pases de codificación que realizará el códec, y \_ g wszVBREnabled, que especifica si el códec usará la codificación de velocidad de bits \_ variable. El número máximo de pases de codificación admitidos por cualquiera de los códecs es dos, por lo que hay cuatro configuraciones distintas para las que puede recuperar códecs, como se muestra en la tabla siguiente.



|    &nbsp;    | Flujo de velocidad de bits constante (CBR) | Secuencia CBR de 2 pases | Flujo de velocidad de bits variable basada en calidad (VBR) | Secuencia de VBR basada en velocidad de bits (restringida o sin restricciones) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | false             | VERDADERO                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Para enumerar los formatos admitidos para un códec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) para encontrar el número de códecs admitidos. A [**continuación, llame a IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) para cada formato. Los índices de formato oscilan entre cero y uno menos que el número total de formatos admitidos. Puede recuperar una descripción del formato llamando a [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Cuando se **usa GetCodecFormatDesc**, no es necesario usar **GetCodecFormat**, ya que ambos métodos recuperan el objeto de configuración de flujo. Los formatos de códec de vídeo no incluyen una descripción. Cada códec de vídeo solo tiene un formato que se usa para todas las secuencias de ese tipo.

Cuando se recupera un formato de códec, se obtiene la [**interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de un objeto de configuración de flujo que contiene la configuración de formato.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de configuración de secuencias de códecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




