---
title: Compatibilidad con marcas de agua
description: Compatibilidad con marcas de agua
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- SDK de Windows Media Format, compatibilidad con marca de agua
- Windows Media Format SDK, marca de agua digital
- Advanced Systems Format (ASF), compatibilidad con marcas de agua
- ASF (formato de sistemas avanzados), compatibilidad con marca de agua
- Advanced Systems Format (ASF), marca de agua digital
- ASF (formato de sistemas avanzados), marca de agua digital
- Windows Media Format SDK, DMO
- Advanced Systems Format (ASF), DMO
- ASF (formato de sistemas avanzados), DMO
- SDK de Windows Media Format, interfaz IWMWatermarkInfo
- Advanced Systems Format (ASF), IWMWatermarkInfo (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMWatermarkInfo
- marcas de agua, acerca de
- marca de agua digital
- Objeto multimedia de DirectX (DMO), acerca de
- DMO (objeto multimedia de DirectX), acerca de
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695558"
---
# <a name="watermarking-support"></a>Compatibilidad con marcas de agua

La marca de agua digital es una manera de insertar derechos de autor u otra información en los datos de una secuencia de medios. Las técnicas para la marca de agua varían mucho de una solución a la siguiente. La forma más sencilla de marca de agua es simplemente agregar una imagen de identificación a cada fotograma de una secuencia de vídeo. Las estaciones de televisión suelen usar esta técnica para insertar un logotipo semitransparente en una esquina inferior de la difusión. Las formas más sofisticadas de la marca de agua digital son imperceptibles para el usuario que ve o escucha el contenido.

El SDK de Windows Media Format admite el uso de [*DMOs*](wmformat-glossary.md)de marca de agua digital. En la práctica, un sistema de marca de agua es muy similar a un códec: toma muestras multimedia, ejecuta algoritmos en los datos y genera los ejemplos alterados. Cuando se especifica un sistema de marcas de agua para una secuencia, el objeto de escritor incluye DMO en el procesamiento de los ejemplos de entrada.

Debe especificar la información de configuración de marca de agua al configurar una secuencia para la marca de agua. Los valores de configuración serán diferentes en función del DMO de marca de agua. La DMO que use debe tener instrucciones que describan los valores de configuración que admite.

Para obtener información sobre la configuración que se usa para especificar un sistema de marca de agua, vea [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Puede programar la aplicación para enumerar el DMOs de marca de agua instalado en el equipo cliente. Para obtener más información, consulte la interfaz [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> </dl>

 

 




