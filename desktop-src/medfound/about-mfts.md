---
description: Acerca de las MTA
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Acerca de las MTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035718"
---
# <a name="about-mfts"></a>Acerca de las MTA

Media Foundation transformaciones (MFT) proporcionan un modelo genérico para procesar datos multimedia. Las MFT se usan para descodificadores, codificadores y procesadores de señales digitales (DSP). En resumen, todo lo que se encuentra en la canalización de medios entre el origen de medios y el receptor de medios es un MFT.

En la mayoría de las aplicaciones, los detalles del procesamiento de datos de MFT se ocultan en capas superiores de la Media Foundation datos. Muchas Media Foundation aplicaciones nunca realizarán una llamada directa a un MFT. Sin embargo, ciertamente es posible hospedar un MFT directamente en la aplicación.

Las MTO son una evolución del modelo de transformación que se introdujo por primera vez con Objetos multimedia DirectX (DMO). De hecho, es relativamente fácil crear una transformación que admita ambos modelos. En comparación con las DDO, los comportamientos necesarios de las MTO se especifican con mayor claridad, lo que facilita la escritura de una implementación correcta. Además, las MTA pueden admitir el procesamiento de vídeo acelerado por hardware.

En este tema se proporciona una breve introducción al modelo de procesamiento de MFT, centrándose en el diseño general en lugar de en llamadas a métodos específicos. Para obtener una descripción paso a paso más detallada, vea Basic MFT Processing Model ( Modelo básico [de procesamiento de MFT).](basic-mft-processing-model.md)

## <a name="streams"></a>Secuencias

Un MFT tiene flujos de entrada y flujos de salida. Los flujos de entrada reciben datos y los flujos de salida generan datos. Por ejemplo, un descodificador tiene un flujo de entrada, que recibe los datos codificados, y un flujo de salida, que genera los datos descodificados.

Las secuencias de un MFT no se representan como objetos COM distintos. En su lugar, cada secuencia tiene un identificador de flujo designado y los métodos de la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) toman los identificadores de flujo como parámetros de entrada.

Algunas MTA tienen un número fijo de secuencias. Por ejemplo, los descodificadores y codificadores normalmente tienen exactamente una entrada y una salida. Otras MTA tienen un número dinámico de secuencias. Si un MFT admite flujos dinámicos, el cliente puede agregar nuevos flujos de entrada. El cliente no puede agregar flujos de salida, pero MFT podría agregar o quitar flujos de salida durante el procesamiento. Por ejemplo, los multiplexores normalmente permiten al cliente agregar flujos de entrada y tener una salida para la secuencia multiplexada. Los demultiplexores son los inversos, con una entrada pero un número dinámico de flujos de salida, en función del contenido del flujo de entrada. En la ilustración siguiente se muestra la diferencia entre multiplexor y demultiplexor.

![diagrama que muestra un codificador/descodificador (1 entrada, 1 salida), un multiplexor (2 entradas, 1 salida) y un demultiplexor (1 entrada, 2 salidas)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Tipos de medios

Cuando se crea por primera vez un MFT, ninguna de las secuencias tiene un formato establecido. Para que MFT pueda procesar los datos, el cliente debe establecer los formatos de las secuencias. Por ejemplo, con un descodificador, el formato de entrada es el formato de compresión utilizado en el archivo de origen original y el formato de salida es un formato sin comprimir, como audio PCM o vídeo RGB. Los formatos de secuencia se describen mediante [tipos de medios](media-types.md).

Dependiendo del estado interno de MFT, podría proporcionar una lista de posibles tipos de medios para cada secuencia. Puede usar esta lista como sugerencia al establecer los tipos de medios. Establecer el tipo de medio en una secuencia puede cambiar la lista de tipos posibles para otra secuencia. Por ejemplo, un descodificador normalmente no puede proporcionar ningún tipo de salida hasta que el cliente establece el tipo de entrada. El tipo de entrada contiene la información que el descodificador necesita para devolver una lista de posibles tipos de salida.

Para establecer el tipo de medio en una secuencia, llame a [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) o [**ASETRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Para obtener la lista de posibles tipos de medios para una secuencia, llame a [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) o [**ASETRANSFORMTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Procesamiento de datos

Después de que el cliente establece los tipos de medios en las secuencias, MFT está listo para procesar los datos. Para que esto suceda, el cliente alterna entre proporcionar datos de entrada al MFT y obtener datos de salida de MFT:

-   Para proporcionar datos de entrada a MFT, llame [**a LANTRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Para extraer los datos de salida de MFT, llame [**a IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

El [**método ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) toma un puntero a un ejemplo multimedia asignado por el cliente. El ejemplo de medios contiene uno o varios búferes y cada búfer contiene datos de entrada para que el MFT lo procese.

El [**método ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) admite dos modelos de asignación diferentes: MFT asigna los búferes de salida o el cliente asigna los búferes de salida. Algunas MFT admiten ambos modelos de asignación, pero no es necesario que un MFT admita ambos. Por ejemplo, un MFT puede requerir que el cliente asigne los búferes de salida. El [**método IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) devuelve información sobre un flujo de salida, incluido el modelo de asignación que admite MFT.

Las MTA están diseñadas para almacenar en búfer el menor número posible de datos, con el fin de minimizar la latencia en la canalización. Por lo tanto, en un momento dado, MFT puede indicar una de las condiciones siguientes:

-   MFT requiere más datos de entrada. En este estado, MFT no puede generar salida hasta que el cliente llame a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) al menos una vez.
-   El MFT no aceptará más entradas hasta que el cliente llame a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) al menos una vez.

Por ejemplo, supongamos que usa un descodificador de vídeo para descodificar una secuencia de vídeo que contiene una combinación de fotogramas clave y fotogramas delta. Inicialmente, el MFT requiere alguna entrada para poder descodificar los fotogramas. El cliente llama [**a ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar el primer fotograma. Supongamos que el primer fotograma es un marco delta (que se muestra en el diagrama siguiente como "P" para el marco de predicción). El descodificador se mantiene en este marco, pero no puede generar ninguna salida hasta que obtiene el siguiente fotograma clave.

![diagrama que muestra el mft que necesita entrada, que apunta a un marco de predicción](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

El cliente sigue llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y finalmente alcanza el siguiente fotograma clave (que se muestra en el diagrama siguiente como "I" para el marco dentro del código). Ahora el descodificador tiene suficientes marcos para empezar a descodificar. En este momento deja de aceptar la entrada y el cliente debe llamar a [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener los marcos descodificados.

![diagrama que muestra un mft que no acepta entrada, que apunta a un marco dentro del código y tres fotogramas predichos](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

El enfoque más sencillo para el cliente es simplemente alternar llamadas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Se describe un algoritmo más sofisticado en el tema [Basic MFT Processing Model](basic-mft-processing-model.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



