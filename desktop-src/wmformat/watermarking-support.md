---
title: Compatibilidad con marcas de agua
description: Compatibilidad con marcas de agua
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows SDK de formato multimedia, compatibilidad con marcas de agua
- Windows SDK de formato multimedia, marca de agua digital
- Formato de sistemas avanzados (ASF), compatibilidad con marcas de agua
- ASF (formato de sistemas avanzados), compatibilidad con la marca de agua
- Formato de sistemas avanzados (ASF), marca de agua digital
- ASF (formato de sistemas avanzados), marca de agua digital
- Windows SDK de formato multimedia, DMO
- Formato de sistemas avanzados (ASF),DMO
- ASF (formato de sistemas avanzados), DMO
- Windows SDK de formato multimedia, interfaz IWMWatermarkInfo
- Formato de sistemas avanzados (ASF), interfaz IWMWatermarkInfo
- ASF (formato de sistemas avanzados), interfaz IWMWatermarkInfo
- marca de agua, acerca de
- marca de agua digital
- Objeto multimedia DirectX (DMO),about
- DMO (objeto multimedia directX),about
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256178"
---
# <a name="watermarking-support"></a>Compatibilidad con marcas de agua

La marca de agua digital es una manera de insertar copyright u otra información en los datos de un flujo multimedia. Las técnicas para la marca de agua varían ampliamente de una solución a la siguiente. La forma más sencilla de marca de agua es simplemente agregar una imagen de identificación a cada fotograma de una secuencia de vídeo. Las estaciones de televisión suelen usar esta técnica para insertar un logotipo semitransparente en una esquina inferior de su difusión. Las formas más sofisticadas de marca de agua digital son imperceptibles para el usuario que ve o escucha el contenido.

El SDK Windows Media Format admite el uso de DDO de [*marca*](wmformat-glossary.md)de agua digital. En la práctica, un sistema de marca de agua es muy similar a un códec: toma ejemplos multimedia, ejecuta algoritmos en los datos y genera los ejemplos modificados. Cuando se especifica un sistema de marca de agua para una secuencia, el objeto writer incluye el DMO en su procesamiento de muestras de entrada.

Debe especificar la información de configuración de la marca de agua al configurar una secuencia para la marca de agua. Los valores de configuración serán diferentes en función de la marca de agua DMO. La DMO que use debe incluir instrucciones que describan los valores de configuración que admite.

Para obtener información sobre la configuración utilizada para especificar un sistema de marca de agua, vea [ **IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Puede programar la aplicación para enumerar las DMO de marca de agua instaladas en el equipo cliente. Para obtener más información, vea la [**interfaz IWMWatermarkInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> </dl>

 

 




