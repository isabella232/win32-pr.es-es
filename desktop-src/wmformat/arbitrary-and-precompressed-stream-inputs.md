---
title: Entradas de flujo arbitrarias y precomprimidas
description: Entradas de flujo arbitrarias y precomprimidas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Formato de sistemas avanzados (ASF), entradas de flujo arbitrarias
- ASF (formato de sistemas avanzados), entradas de flujo arbitrarias
- perfiles, entradas de flujo arbitrarias
- códecs, entradas de flujo arbitrarias
- Formato de sistemas avanzados (ASF), entradas de flujo precomprimidas
- ASF (formato de sistemas avanzados), entradas de flujo precomprimidas
- perfiles, entradas de flujo precomprimidas
- códecs, entradas de flujo precomprimidas
- entradas de flujo precomprimidas
- entradas de flujo arbitrarias
- streams,arbitrary stream inputs
- streams,precompressed stream inputs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0129362e8dc01b7ccf3faabbf10e22ffd4eccc082782796059b3cf4578c33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448275"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Entradas de flujo arbitrarias y precomprimidas

Solo las entradas que se van a comprimir mediante uno de los códecs Windows media tienen varias entradas posibles. Los otros tipos de entradas posibles son entradas arbitrarias y entradas precomprimidas. Los requisitos de los formatos de entrada para estos tipos se describen en esta sección.

## <a name="arbitrary-stream-inputs"></a>Entradas de flujo arbitrarias

Las entradas para tipos de secuencia arbitrarios son las mismas que los formatos de secuencia descritos en el perfil. No debe tener que establecer formatos de entrada para estos tipos.

## <a name="precompressed-stream-inputs"></a>Entradas de flujo precomprimidas

Al copiar una secuencia de un archivo a otro, se pasan ejemplos que ya están comprimidos. En este caso, debe establecer el objeto de propiedades de entrada en **NULL** para informar al escritor de que no necesita validar los datos que está pasando. Para establecer el formato de entrada en **NULL,** llame [**a IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pase **NULL** como segundo parámetro. Al llamar a este método con **un parámetro NULL,** debe realizar la llamada antes de llamar a [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Al usar secuencias precomprimidas, debe copiar manualmente la información del códec en el encabezado de archivo antes de escribir. Para obtener la información del códec, llame a [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector. Seleccione la información del códec que coincida con la configuración de secuencia de la secuencia precomprimida. A continuación, establezca la información del códec en el escritor mediante una llamada [**a IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 




