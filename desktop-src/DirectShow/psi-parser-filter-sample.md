---
description: Ejemplo de filtro del analizador de PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Ejemplo de filtro del analizador de PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160112"
---
# <a name="psi-parser-filter-sample"></a>Ejemplo de filtro del analizador de PSI

## <a name="description"></a>Descripción

El filtro Analizador de PSI recibe información específica del programa (PSI) de un flujo de transporte MPEG-2 y extrae información del programa de la tabla de asociación de programas (PAT) y las tablas de asignación de programa (PMT). Esta información permite a una aplicación configurar el demultiplexor MPEG-2. El filtro admite una interfaz personalizada, [**IMpeg2PsiParser,**](impeg2psiparser.md)para recuperar la información de PSI.

Este filtro está diseñado para dispositivos MPEG-2, como IEEE 1394 de vídeo MPEG-2 y dispositivos D-VHS. Consulte [Controlador MSTape para](mstape-driver.md) obtener más información. Los orígenes de difusión de televisión digital deben usar un filtro TIF para obtener información del programa.

## <a name="usage"></a>Uso

Puede probar el filtro del analizador de PSI en GraphEdit de la siguiente manera:

1.  Inicie GraphEdit.
2.  Inserte un origen de transporte MPEG-2. Las cámaras MPEG-2 y los dispositivos D-VHS aparecen como "Dispositivo de subunidad de cinta de Microsoft AV/C" en la categoría Orígenes de captura de vídeo.
3.  Conectar filtro de origen al filtro Demultiplexer MPEG-2.
4.  Use la página de propiedades de demux para crear un pin de salida con un tipo de medio "MPEG-2 PSI". Este pin entregará las secciones PAT y PMT.
5.  Use la página de propiedades de demux para asignar pid 0x00 al pin de salida. Establezca el tipo de contenido en "Mpeg2 PSI Sections".
6.  Conectar el pin de salida de demux al analizador PSI, como se muestra en el diagrama siguiente.

    ![gráfico de filtro de analizador psi](images/psi-parser.png)

7.  Ejecute el gráfico para alimentar los datos de PSI al filtro del analizador de PSI. A medida que el filtro descodifica las secciones PAT, asigna automáticamente los PID de PMT al mismo pin de salida en demux, de modo que recibe las secciones pmt.
8.  Use la página de propiedades Analizador de PSI para seleccionar un número de programa. La lista de secuencias elementales de la página de propiedades mostrará el PID y el tipo de secuencia asociados a cada flujo básico del programa seleccionado. La página de propiedades está diseñada para reconocer los tipos de flujo definidos en ISO/IEC 13818-1.
9.  Escriba el número de PID de audio en el **cuadro de** edición PID de audio y el número de PID de vídeo en el cuadro de **edición PID** de vídeo.
10. Haga clic en **el botón Ver** programa. El analizador de PSI configurará los pines de salida en demux para que coincidan con la información del flujo de programa y represente los pines.

> [!Note]  
> La página de propiedades Analizador de PSI se proporciona para facilitar las pruebas y para proporcionar código de ejemplo que configura el demultiplexor MPEG-2. No se recomienda que las aplicaciones lo usen. Las aplicaciones deben configurar la demux mediante programación.

 

Para usar el filtro psi parser en una aplicación, empiece por compilar el gráfico de filtro desde el origen MPEG-2 a la demux MPEG-2. El código de este paso no se muestra aquí, porque la configuración exacta del grafo dependerá del origen.

A continuación, cree un pin de salida en demux para los datos psi. Asigne el 0x00 PID, que está reservado para las secciones PAT, a este pin, como se muestra en el código siguiente:


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



Para obtener más información, [vea Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).

Agregue el filtro psi parser al gráfico y conéctelo al pin de salida en demux. Consulte el analizador de PSI para la [**interfaz IMpeg2PsiParser.**](impeg2psiparser.md) Ahora, ejecute el gráfico y espere los eventos EC PROGRAM CHANGED, que señalan \_ una nueva sección PAT o \_ PMT. Este evento es un evento personalizado definido por el filtro de analizador PSI. Cuando reciba un evento EC PROGRAM CHANGED, puede obtener la información de PSI disponible llamando a los métodos \_ \_ **IMpeg2PsiParser.** En esta sección se describen los métodos que necesitará con más frecuencia.

Para obtener el número de programas, use el [**método IMpeg2PsiParser::GetCountOfPrograms:**](impeg2psiparser-getcountofprograms.md)


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Para obtener el número de programa de un programa específico, use el [**método IMpeg2PsiParser::GetRecordProgramNumber:**](impeg2psiparser-getrecordprogramnumber.md)


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



El número de programa se usa para obtener las entradas de PMT para programas individuales. Para obtener el número de secuencias elementales de un programa, use el [**método GetCountOfElementaryStreams:**](impeg2psiparser-getcountofelementarystreams.md)


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Para cada secuencia elemental, el método [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) devuelve el PID y el método [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) devuelve el tipo de secuencia:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



El PID y el tipo de secuencia le permiten configurar nuevas clavijas de salida en el demultiplexor MPEG-2. Esto puede requerir cierto conocimiento del origen original. Por ejemplo, ISO/IEC 13818-1 define los tipos de secuencias de 0x80 a 0xFF como "usuario privado", pero otros estándares basados en MPEG-2 pueden asignar otros significados a estos tipos.

El demultiplexador MPEG-2 puede crear nuevos pines y nuevas asignaciones de PID mientras se ejecuta el gráfico, pero debe detener el gráfico para conectar los pines.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente de [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ PSIParser.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> <dt>

[**IMpeg2PsiParser (interfaz)**](impeg2psiparser.md)
</dt> </dl>

 

 
