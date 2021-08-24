---
description: Configuración del objeto divisor de ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configuración del objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7068f2c869f6c73447b3341baee7221cdf8efbacec47ecdfa3a584bfb456f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606155"
---
# <a name="configuring-the-asf-splitter-object"></a>Configuración del objeto divisor de ASF

El objeto *divisor* ASF es un objeto de capa WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistemas avanzados (ASF). Después de crear e inicializar el divisor para analizar el objeto de datos de ASF de un archivo multimedia, el divisor debe configurarse para generar ejemplos para secuencias específicas. Llame [**a IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para seleccionar las secuencias necesarias.

Opcionalmente, una aplicación también puede configurarla para generar ejemplos en orden inverso o generar ejemplos para el contenido protegido. Para establecer estas opciones, llame a [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) y pase la combinación bit a bit necesaria de las marcas admitidas. Antes de llamar a este método, el cliente debe completar correctamente la llamada [**a IMFASFSplitter::Initialize;**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) De lo contrario, Se produce un error en **SetFlags** con el código de error **MF E NOT \_ \_ \_ INITIALIZED.** Para obtener información sobre cómo inicializar el divisor, vea [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).

Para comprobar si esta marca está establecida actualmente en el divisor, llame a [**IMFASFSplitter::GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Selección de Secuencias para el análisis

Durante el proceso de inicialización a través de la llamada [**a IMFASFSplitter::Initialize,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) el divisor detecta el número de secuencias y los identificadores de flujo en el archivo ASF. De forma predeterminada, el divisor no selecciona ninguna secuencia. La aplicación debe seleccionar las secuencias llamando a [**IMFASFSplitter::SelectStreams.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) Este método toma una matriz de números de secuencia. Para obtener el número de secuencia de una secuencia, llame a [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) en el perfil de ASF o llame a [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) en el descriptor de flujo. (Puede obtener el perfil de ASF y el descriptor de flujo del objeto ContentInfo). Si el cliente pasa un número de secuencia que el divisor no reconoce, se produce un error **\_ \_ INVALIDSTREAMNUMBER de MF E.**

Al [**llamar a SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) se borran las selecciones anteriores. No se selecciona ninguna secuencia que no se especifique en la matriz. Para obtener una lista de secuencias que están seleccionadas actualmente, llame a [**IMFASFSplitter::GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Este método toma un puntero a una matriz, que el método rellena con los números de secuencia. Si el tamaño de la matriz es menor que el número de secuencias seleccionadas, el método produce el error **\_ MF E \_ BUFFERTOOSMALL.** En este caso, el método devuelve el número de secuencias seleccionadas en el *parámetro pwNumStreams.* A continuación, puede usar este número para asignar una matriz del tamaño correcto y llamar al método de nuevo.

Para obtener código de ejemplo, vea "Select a Stream for Parsing" (Seleccionar una secuencia para analizar) [en Tutorial: Lectura de un archivo ASF.](tutorial--reading-an-asf-file.md)

## <a name="reverse-playback-setting"></a>Configuración de reproducción inversa

Durante el proceso de inicialización del divisor, determina si el contenido de ASF admite la reproducción inversa. Si es así, el divisor se puede configurar para generar muestras en orden inverso estableciendo la marca **MFASF \_ SPLITTER \_ REVERSE.** Si el contenido no admite la reproducción inversa, [**MFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) devuelve **MF E \_ \_ INVALIDREQUEST**, pero la marca se establece en el divisor.

Si el divisor está configurado para analizarse en la dirección inversa, el divisor siempre empieza a analizarse al final del búfer que contiene el objeto de datos de ASF. Por lo tanto, para el análisis inverso, el desplazamiento de datos y la longitud de los datos que se va a analizar deben establecerse correctamente. Para obtener información sobre cómo establecer los valores correctos, vea Generar ejemplos de flujo a partir de [un objeto de datos asf existente.](generating-stream-samples-from-an-existing-asf-data-object.md)

## <a name="protected-content-setting"></a>Configuración de contenido protegido

El divisor se puede configurar para que funcione con contenido de cifrado de nivel de paquete estableciendo **MFASF \_ SPLITTER \_ WMDRM** a través de [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). Esto indica al divisor que entregue ejemplos de contenido protegido por Windows Media Digital Rights Management (DRM). Cuando se establece esta marca, los ejemplos generados por el divisor contienen la información necesaria para descifrar los datos multimedia y reconstruir los fotogramas, como el atributo [**MFSampleExtension \_ PacketCrossOffsets.**](mfsampleextension-packetcrossoffsets-attribute.md) Este atributo es un blob que contiene una matriz **de DWORD.** Cada **DWORD proporciona** los límites de carga del marco con respecto al principio del marco. Si este atributo no está presente, el marco se incluye en una sola carga. Normalmente, los ejemplos generados por el divisor contienen varios búferes multimedia; la aplicación puede copiar todos los búferes en un búfer contiguo llamando a [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). El búfer resultante contiene el marco y el valor del atributo contiene desplazamientos en este búfer.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> </dl>

 

 



