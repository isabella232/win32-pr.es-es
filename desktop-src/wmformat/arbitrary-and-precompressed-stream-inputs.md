---
title: Entradas de secuencias arbitrarias y precomprimidas
description: Entradas de secuencias arbitrarias y precomprimidas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), entradas de secuencias arbitrarias
- ASF (formato de sistemas avanzados), entradas de secuencias arbitrarias
- perfiles, entradas de secuencias arbitrarias
- códecs, entradas de secuencias arbitrarias
- Advanced Systems Format (ASF), entradas de secuencias precomprimidas
- ASF (formato de sistemas avanzados), entradas de secuencias precomprimidas
- perfiles, entradas de secuencias precomprimidas
- códecs, entradas de secuencias precomprimidas
- entradas de secuencias precomprimidas
- entradas de secuencias arbitrarias
- secuencias, entradas de secuencias arbitrarias
- secuencias, entradas de secuencias precomprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105704913"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a>Entradas de secuencias arbitrarias y precomprimidas

Solo las entradas que se van a comprimir con uno de los códecs de Windows Media tienen varias entradas posibles. Los otros tipos de entradas posibles son entradas arbitrarias y entradas precomprimidas. En esta sección se describen los requisitos para los formatos de entrada de estos tipos.

## <a name="arbitrary-stream-inputs"></a>Entradas de secuencias arbitrarias

Las entradas de tipos de flujo arbitrarios son las mismas que los formatos de secuencia descritos en el perfil. No debe tener que establecer formatos de entrada para estos tipos.

## <a name="precompressed-stream-inputs"></a>Entradas de secuencias precomprimidas

Cuando se copia una secuencia de un archivo a otro, se pasan ejemplos que ya están comprimidos. En este caso, debe establecer el objeto de propiedades de entrada en **null** para informar al escritor de que no necesita validar los datos que está pasando. Para establecer el formato de entrada en **null**, llame a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pase **null** como segundo parámetro. Al llamar a este método con un parámetro **null** , debe realizar la llamada antes de llamar a [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Al utilizar secuencias precomprimidas, debe copiar manualmente la información del códec en el encabezado del archivo antes de la escritura. Para obtener la información del códec, llame a [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) y [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector. Seleccione la información del códec que coincida con la configuración de la secuencia precomprimida. A continuación, establezca la información del códec en el escritor llamando a [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con entradas**](working-with-inputs.md)
</dt> </dl>

 

 




