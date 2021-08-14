---
title: Funcionamiento del ejemplo de eco
description: Funcionamiento del ejemplo de eco
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Reproductor de Windows Media complementos, Información general del ejemplo de eco
- complementos, información general de ejemplo de eco
- complementos de procesamiento de señales digitales, información general de ejemplo de eco
- Complementos DE DSP, Información general del ejemplo de eco
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290cb56bbf1900dbcc09874213490f80cdc3af179ff243a2867bb232c3bb85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338960"
---
# <a name="how-the-echo-sample-works"></a>Funcionamiento del ejemplo de eco

El código crea el efecto de eco asignando un búfer lo suficientemente grande como para contener exactamente la cantidad de datos de audio que se pueden representar en el período de tiempo especificado por el valor de tiempo de retraso. El tamaño del búfer se calcula, en bytes, mediante la fórmula siguiente:

buffer size = delay time \* sample rate /1000 \* block alignment

El tiempo de retraso es en milisegundos. Los valores de frecuencia de muestreo y alineación de bloques se dan en una estructura DESATEX. La frecuencia de muestreo es en muestras por segundo; dividir por 1000 produce muestras por milisegundo. La alineación del bloque es igual al producto del número de canales (1 para mono, 2 para estéreo) y el número de bits por muestra (8 o 16) dividido entre 8 (bits por byte).

Además de la variable de puntero que apunta al responsable del búfer de retraso, el código crea un puntero móvil que recorre los datos del búfer en sincronización con el bucle de procesamiento de la función **DoProcessOutput.** Cuando el puntero móvil alcanza el final del búfer de retraso, vuelve al extremo del búfer. Un búfer usado de esta manera se denomina búfer circular.

Una vez que existe el búfer de retraso y Reproductor de Windows Media ha asignado un búfer de entrada para proporcionar datos de audio y un búfer de salida para recibir datos de audio procesados, el procesamiento de eco continúa de la siguiente forma:

1.  Escriba un bucle que permita el procesamiento de cada muestra de audio en el búfer de entrada.
2.  Recuperar un ejemplo del búfer de entrada. A continuación, mueva el puntero de búfer de entrada hacia delante al ejemplo siguiente para prepararse para la siguiente iteración del bucle.
3.  Recuperar un ejemplo del búfer de retraso.
4.  Copie el ejemplo del búfer de entrada en la misma ubicación del búfer de retraso del que se recuperó la última muestra de retraso.
5.  Mueva el puntero de búfer de retraso hacia delante al ejemplo siguiente. Si el puntero se mueve más allá del final del búfer, muévolo al extremo del búfer.
6.  Combine el ejemplo del búfer de entrada con el ejemplo del búfer de retraso.
7.  Copie el resultado en el búfer de salida. A continuación, mueva el puntero del búfer de salida hacia delante a la unidad siguiente para prepararse para la siguiente iteración del bucle.
8.  Repita la repetición hasta que se procese todas las muestras.

Cuando se copia un ejemplo de entrada recuperado en el paso 2 en el búfer de retraso en el paso 4, permanece allí hasta que el puntero móvil atraviesa cada muestra en el búfer de retraso y, por último, vuelve a la misma posición. Dado que el tamaño del búfer de retraso está diseñado para corresponder al tiempo de retraso, el tiempo transcurrido entre la muestra que se copia en el búfer de retraso y la muestra que se recupera una vez más es igual al retraso especificado (más cualquier latencia introducida por el procesamiento real).

Cuando se inicia una secuencia, no se generan datos de retraso hasta que transcurre el tiempo de retraso. Por lo tanto, es importante que el búfer de retraso inicialmente contenga silencio. Si el búfer de retraso contiene datos aleatorios, el usuario escuchará ruido blanco hasta que el complemento genere suficientes datos de retraso para sobrescribir todo el búfer de retraso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general del ejemplo de eco**](echo-sample-overview.md)
</dt> </dl>

 

 




