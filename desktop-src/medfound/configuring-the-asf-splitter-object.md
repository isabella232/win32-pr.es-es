---
description: Configurar el objeto divisor de ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configurar el objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f27885e602dd52012808d330d997f9b7a7e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153666"
---
# <a name="configuring-the-asf-splitter-object"></a>Configurar el objeto divisor de ASF

El objeto de *separador* ASF es un objeto de capa WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF). Una vez creado e inicializado el divisor para analizar el objeto de datos ASF de un archivo multimedia, el divisor debe configurarse para generar ejemplos para flujos concretos. Llame a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para seleccionar los flujos necesarios.

Opcionalmente, una aplicación también puede configurarla para generar ejemplos en orden inverso o generar ejemplos para contenido protegido. Para establecer estas opciones, llame a [**IMFASFSplitter:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) y pase la combinación bit a bit necesaria de las marcas admitidas. Antes de llamar a este método, el cliente debe completar la llamada a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) correctamente; en caso contrario, se produce un error en **SetFlags** con el código de error de **MF \_ E \_ no \_ inicializado** . Para obtener información sobre cómo inicializar el divisor, vea [crear el objeto divisor de ASF](creating-the-asf-splitter-object.md).

Para comprobar si esta marca está establecida actualmente en el divisor, llame a [**IMFASFSplitter:: GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Seleccionar secuencias para el análisis

Durante el proceso de inicialización a través de la llamada a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) , el divisor detecta el número de secuencias y los identificadores de flujo en el archivo ASF. De forma predeterminada, el divisor selecciona ningún flujo. La aplicación debe seleccionar los flujos mediante una llamada a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams). Este método toma una matriz de números de secuencia. Para obtener el número de secuencia de una secuencia, llame a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) en el perfil ASF o llame a [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) en el descriptor de flujo. (Puede obtener el perfil ASF y el descriptor de secuencia del objeto ContentInfo). Si el cliente pasa un número de secuencia que el divisor no reconoce, se produce un error **de \_ \_ INVALIDSTREAMNUMBER MF E** .

Al llamar a [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) se borran las selecciones anteriores. No se selecciona ningún flujo que no se haya especificado en la matriz. Para obtener una lista de las secuencias que están seleccionadas actualmente, llame a [**IMFASFSplitter:: GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Este método toma un puntero a una matriz, que el método rellena con los números de secuencia. Si el tamaño de la matriz es menor que el número de secuencias seleccionadas, se produce un error en el método con el error **MF \_ E \_ BUFFERTOOSMALL** . En este caso, el método devuelve el número de secuencias seleccionadas en el parámetro *pwNumStreams* . Después, puede usar este número para asignar una matriz del tamaño correcto y volver a llamar al método.

Para obtener código de ejemplo, vea "seleccionar una secuencia para el análisis" en [Tutorial: leer un archivo ASF](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Configuración de reproducción inversa

Durante el proceso de inicialización del divisor, determina si el contenido ASF admite la reproducción inversa. Si es así, el divisor puede configurarse para generar ejemplos en orden inverso estableciendo la marca de **\_ \_ reverso del divisor MFASF** . Si el contenido no admite la reproducción inversa, [**IMFASFSplitter:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) devuelve **MF \_ E \_ INVALIDREQUEST**, pero la marca se establece en el divisor.

Si el divisor está configurado para analizar en dirección inversa, el divisor siempre comienza el análisis al final del búfer que contiene el objeto de datos ASF. Por lo tanto, para el análisis inverso, el desplazamiento de los datos y la longitud de los datos que se van a analizar deben establecerse de forma adecuada. Para obtener información acerca de cómo establecer los valores correctos, vea [generar ejemplos de secuencias a partir de un objeto de datos ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).

## <a name="protected-content-setting"></a>Configuración de contenido protegido

El divisor puede configurarse para trabajar con el contenido de cifrado de nivel de paquete estableciendo el **\_ divisor de MFASF \_ WMDRM** a través de [**IMFASFSplitter:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). Esto indica al divisor que proporcione ejemplos de contenido protegido por Rights Management digital (DRM) de Windows Media. Cuando se establece esta marca, los ejemplos generados por el divisor contienen información necesaria para descifrar los datos multimedia y reconstruir los fotogramas, como el atributo [**\_ PacketCrossOffsets de MFSampleExtension**](mfsampleextension-packetcrossoffsets-attribute.md) . Este atributo es un BLOB que contiene una matriz de **DWORD** s. Cada **DWORD** proporciona los límites de carga para el marco con respecto al principio del marco. Si este atributo no está presente, el marco se incluye en una sola carga. Normalmente, los ejemplos generados por el divisor contienen varios búferes multimedia, la aplicación puede copiar todos los búferes en un búfer contiguo mediante una llamada a [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). El búfer resultante contiene el marco y el valor del atributo contiene los desplazamientos en este búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Divisor ASF](asf-splitter.md)
</dt> </dl>

 

 



