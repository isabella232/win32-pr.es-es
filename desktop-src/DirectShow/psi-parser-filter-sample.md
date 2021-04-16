---
description: Ejemplo de filtro de analizador de PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Ejemplo de filtro de analizador de PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104552732"
---
# <a name="psi-parser-filter-sample"></a>Ejemplo de filtro de analizador de PSI

## <a name="description"></a>Descripción

El filtro del analizador de PSI recibe información específica del programa (PSI) de una secuencia de transporte MPEG-2 y extrae información del programa de la tabla de Asociación de programas (PAT) y de las tablas de mapa de programa (PMT). Esta información permite a una aplicación configurar el desmultiplexador MPEG-2. El filtro admite una interfaz personalizada, [**IMpeg2PsiParser**](impeg2psiparser.md), para recuperar la información de PSI.

Este filtro está diseñado para dispositivos MPEG-2, como camascopios IEEE 1394 MPEG-2 y dispositivos D-VHS. Consulte [controlador MSTape](mstape-driver.md) para obtener más información. Los orígenes de difusión de televisión digital deben usar un filtro TIF para obtener información del programa.

## <a name="usage"></a>Uso

Puede probar el filtro del analizador de PSI en GraphEdit como se indica a continuación:

1.  Inicie GraphEdit.
2.  Inserte un origen de transporte MPEG-2. Las videocámaras MPEG-2 y los dispositivos D-VHS aparecen como "dispositivo de subunidad de cinta AV/C de Microsoft" en la categoría de orígenes de captura de vídeo.
3.  Conecte el filtro de origen al filtro de demultiplexador MPEG-2.
4.  Use la página de propiedades de Demux para crear un PIN de salida con un tipo de medio "MPEG-2 PSI". Este pin proporcionará las secciones PAT y PMT.
5.  Use la página de propiedades Demux para asignar el PID 0x00 al terminal de salida. Establezca el tipo de contenido en "secciones de PSI de MPEG2".
6.  Conecte el PIN de salida de Demux al analizador de PSI, tal como se muestra en el diagrama siguiente.

    ![gráfico de filtro del analizador de PSI](images/psi-parser.png)

7.  Ejecute el gráfico para alimentar los datos de la PSI al filtro del analizador de PSI. A medida que el filtro descodifica las secciones PAT, asigna automáticamente los PID de pago al mismo pin de salida en el Demux, de modo que recibe las secciones PMT.
8.  Use la página de propiedades del analizador de PSI para seleccionar un número de programa. La lista de secuencias elementales de la página de propiedades mostrará el PID y el tipo de secuencia asociados a cada flujo elemental en el programa seleccionado. La página de propiedades está diseñada para reconocer los tipos de secuencia definidos en ISO/IEC 13818-1.
9.  Escriba el número de PID de audio en el cuadro de edición **PID de audio** y el número de PID de vídeo en el cuadro de edición **PID de vídeo** .
10. Haga clic en el botón **Ver programa** . El analizador de PSI configurará los pin de salida en Demux para que coincidan con la información de la secuencia de programa y representen los pin.

> [!Note]  
> La página de propiedades del analizador de PSI se proporciona para facilitar la realización de pruebas y proporcionar código de ejemplo que configura el desmultiplexador MPEG-2. No se recomienda para las aplicaciones. Las aplicaciones deben configurar el Demux mediante programación.

 

Para usar el filtro del analizador PSI en una aplicación, empiece por crear el gráfico de filtros desde el origen MPEG-2 hasta el Demux MPEG-2. Aquí no se muestra el código de este paso, ya que la configuración exacta del gráfico dependerá del origen.

A continuación, cree un PIN de salida en Demux para los datos de PSI. Asigne el PID 0x00, que está reservado para las secciones PAT, a este pin, como se muestra en el código siguiente:


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



Para obtener más información, consulte [uso del demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md).

Agregue el filtro de analizador de PSI al gráfico y conéctelo al pin de salida en el Demux. Consulte el analizador de PSI para la interfaz [**IMpeg2PsiParser**](impeg2psiparser.md) . Ahora ejecute el gráfico y espere a \_ que se \_ hayan cambiado los eventos del programa EC, que señalan una nueva sección Pat o PMT. Este evento es un evento personalizado definido por el filtro del analizador PSI. Cuando reciba un evento de \_ cambio de programa de EC \_ , puede obtener la información de PSI disponible llamando a métodos **IMpeg2PsiParser** . En esta sección se describen los métodos que necesitará con más frecuencia.

Para obtener el número de programas, use el método [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Para obtener el número de programa para un programa específico, use el método [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



El número de programa se usa para obtener las entradas de pago de programas individuales. Para obtener el número de flujos elementales en un programa, use el método [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Para cada flujo elemental, el método [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) devuelve el PID y el método [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) devuelve el tipo de flujo:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



El PID y el tipo de secuencia permiten configurar nuevas clavijas de salida en el demultiplexador MPEG-2. Esto puede requerir cierto conocimiento del origen original. Por ejemplo, ISO/IEC 13818-1 define tipos de secuencia de 0x80 a 0xFF como "usuario privado", pero otros estándares basados en MPEG-2 pueden asignar otros significados a estos tipos.

El demultiplexador MPEG-2 puede crear nuevos PIN y nuevas asignaciones de PID mientras el gráfico se está ejecutando, pero debe detener el gráfico para conectar los pin.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ PSIParser.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> <dt>

[**Interfaz IMpeg2PsiParser**](impeg2psiparser.md)
</dt> </dl>

 

 
