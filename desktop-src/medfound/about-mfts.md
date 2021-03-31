---
description: Acerca de MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Acerca de MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09adce4bc93c110cf98e4fd8ed427ffcd009c3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908043"
---
# <a name="about-mfts"></a>Acerca de MFTs

Media Foundation transformaciones (MFTs) proporcionan un modelo genérico para procesar los datos multimedia. MFTs se usan para descodificadores, codificadores y procesadores de señal digital (DSP). En Resumen, todo lo que se encuentra en la canalización multimedia entre el origen multimedia y el receptor multimedia es un MFT.

Para la mayoría de las aplicaciones, los detalles del procesamiento de datos de MFT están ocultos en los niveles superiores de la arquitectura de Media Foundation. Muchas aplicaciones de Media Foundation nunca realizarán una llamada directa a una MFT. Sin embargo, es ciertamente posible hospedar un MFT directamente en la aplicación.

MFTs son una evolución del modelo de transformación que se presentó por primera vez con objetos de DirectX media (DMOs). De hecho, es relativamente fácil crear una transformación que admita ambos modelos. En comparación con DMOs, los comportamientos necesarios de MFTs se especifican con más claridad, lo que facilita la escritura de una implementación correcta. Además, MFTs puede admitir el procesamiento de vídeo acelerado por hardware.

En este tema se proporciona una breve introducción al modelo de procesamiento de MFT, centrándose en el diseño general en lugar de llamadas a métodos específicos. Para obtener una descripción paso a paso más detallada, vea modelo de [procesamiento de MFT básico](basic-mft-processing-model.md).

## <a name="streams"></a>Secuencias

Una MFT tiene flujos de entrada y flujos de salida. Los flujos de entrada reciben datos y los flujos de salida generan datos. Por ejemplo, un descodificador tiene un flujo de entrada, que recibe los datos codificados y un flujo de salida, que genera los datos descodificados.

Los flujos de una MFT no se representan como objetos COM distintos. En su lugar, cada flujo tiene un identificador de flujo designado y los métodos de la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) toman los identificadores de secuencia como parámetros de entrada.

Algunos MFTs tienen un número fijo de flujos. Por ejemplo, los descodificadores y codificadores suelen tener exactamente una entrada y una salida. Otros MFTs tienen un número dinámico de flujos. Si una MFT admite secuencias dinámicas, el cliente puede agregar nuevos flujos de entrada. El cliente no puede Agregar flujos de salida, pero el MFT podría agregar o quitar flujos de salida durante el procesamiento. Por ejemplo, los multiplexores normalmente permiten al cliente agregar flujos de entrada y tener una salida para la secuencia multiplexada. Los demultiplexadores son los inversos, con una entrada, pero un número dinámico de flujos de salida, en función del contenido del flujo de entrada. En la ilustración siguiente se muestra la diferencia entre multiplexor y separador.

![diagrama que muestra un codificador/descodificador (1 entrada, 1 salida), un multiplexor (2 entradas, 1 salida) y un demultiplexador (1 entrada, 2 salidas)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Tipos de medios

Cuando se crea por primera vez un MFT, ninguno de los flujos tiene un formato establecido. Para que la MFT pueda procesar los datos, el cliente debe establecer los formatos de las secuencias. Por ejemplo, con un descodificador, el formato de entrada es el formato de compresión utilizado en el archivo de código fuente original y el formato de salida es un formato sin comprimir, como audio PCM o vídeo RGB. Los formatos de secuencia se describen mediante [tipos de medios](media-types.md).

Dependiendo del estado interno de la MFT, podría proporcionar una lista de posibles tipos de medios para cada flujo. Puede usar esta lista como una sugerencia al establecer los tipos de medios. Si se establece el tipo de medio en una secuencia, se puede cambiar la lista de posibles tipos de otro flujo. Por ejemplo, un descodificador normalmente no puede proporcionar ningún tipo de salida hasta que el cliente establece el tipo de entrada. El tipo de entrada contiene la información que el descodificador necesita para devolver una lista de posibles tipos de salida.

Para establecer el tipo de medio en una secuencia, llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) o [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Para obtener la lista de los posibles tipos de medios de una secuencia, llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) o [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Procesamiento de datos

Después de que el cliente establezca los tipos de medios en las secuencias, la MFT está lista para procesar los datos. Para que esto suceda, el cliente alterna entre proporcionar datos de entrada al MFT y obtener los datos de salida de la MFT:

-   Para proporcionar datos de entrada a la MFT, llame a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Para extraer los datos de salida de MFT, llame a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

El método [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) toma un puntero a un ejemplo multimedia asignado por el cliente. El ejemplo multimedia contiene uno o más búferes y cada búfer contiene datos de entrada para que los procese el MFT.

El método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) admite dos modelos de asignación diferentes: el MFT asigna los búferes de salida o el cliente asigna los búferes de salida. Algunos MFTs admiten ambos modelos de asignación, pero no es necesario que un MFT admita ambos. Por ejemplo, un MFT podría requerir que el cliente asignara los búferes de salida. El método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve información acerca de un flujo de salida, incluido el modelo de asignación que la MFT admite.

MFTs están diseñados para almacenar en búfer los datos mínimos posibles, con el fin de minimizar la latencia en la canalización. Por lo tanto, en un momento dado, la MFT puede indicar una de las siguientes condiciones:

-   La MFT requiere más datos de entrada. En este estado, la MFT no puede producir la salida hasta que el cliente llame a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) al menos una vez.
-   La MFT no aceptará más entradas hasta que el cliente llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) al menos una vez.

Por ejemplo, supongamos que usa un descodificador de vídeo para descodificar una secuencia de vídeo que contiene una combinación de fotogramas clave y fotogramas Delta. Inicialmente, la MFT requiere algunos datos para poder descodificar los fotogramas. El cliente llama a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para proporcionar el primer fotograma. Supongamos que el primer fotograma es un fotograma Delta (se muestra en el siguiente diagrama como "P" para el marco de predicción). El descodificador retiene en este fotograma, pero no puede producir ningún resultado hasta que obtiene el siguiente fotograma clave.

![diagrama que muestra la MFT que necesita entrada y apunta a un marco de predicción](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

El cliente sigue llamando a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y, finalmente, alcanza el fotograma clave siguiente (que se muestra en el siguiente diagrama como "I" para el marco dentro de la codificación). Ahora el descodificador tiene suficientes fotogramas para iniciar la descodificación. En este punto, deja de aceptar la entrada y el cliente debe llamar a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener los fotogramas descodificados.

![diagrama que muestra un MFT que no acepta entradas, que apunta a un marco dentro de la codificación y tres marcos predichos](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

El enfoque más sencillo para el cliente es simplemente llamadas alternativas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). En el tema [modelo de procesamiento de MFT básico](basic-mft-processing-model.md)se describe un algoritmo más sofisticado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



