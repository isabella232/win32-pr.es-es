---
title: Cómo funciona el ejemplo echo
description: Cómo funciona el ejemplo echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Complementos de Media Player de Windows, información general de ejemplo de eco
- complementos, información general de ejemplo de eco
- Complementos de procesamiento de señal digital, información general de ejemplo de eco
- Complementos DSP, información general de ejemplo de eco
- Ejemplo de complemento DSP de eco, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695342"
---
# <a name="how-the-echo-sample-works"></a>Cómo funciona el ejemplo echo

El código crea el efecto de eco asignando un búfer lo suficientemente grande como para contener exactamente la cantidad de datos de audio que se pueden representar en el intervalo de tiempo especificado por el valor de tiempo de retraso. El tamaño del búfer se calcula, en bytes, mediante la siguiente fórmula:

tamaño de búfer = frecuencia de muestreo de tiempo de retraso \* / \* alineación de bloque 1000

El tiempo de retardo está en milisegundos. La velocidad de muestreo y los valores de alineación de bloque se proporcionan en una estructura WAVEFORMATEX. La velocidad de muestreo es en muestras por segundo; la división por 1000 produce muestras por milisegundo. La alineación de bloque es igual al producto del número de canales (1 para mono, 2 para estéreo) y el número de bits por muestra (8 o 16) dividido entre 8 (bits por byte).

Además de la variable de puntero que apunta al encabezado del búfer de retraso, el código crea un puntero movible que recorre los datos del búfer en sincronización con el bucle de procesamiento en la función **DoProcessOutput** . Cuando el puntero movible alcanza el final del búfer de retraso, vuelve al encabezado del búfer. Un búfer que se usa de esta manera se denomina búfer circular.

Una vez que el búfer de retraso existe y Windows Media Player ha asignado un búfer de entrada para proporcionar datos de audio y un búfer de salida para recibir los datos de audio procesados, el procesamiento de eco es similar al siguiente:

1.  Escriba un bucle que permita el procesamiento de cada ejemplo de audio en el búfer de entrada.
2.  Recupera un ejemplo del búfer de entrada. A continuación, mueva el puntero de búfer de entrada hacia delante hasta el ejemplo siguiente para preparar la siguiente iteración del bucle.
3.  Recupera un ejemplo del búfer de retraso.
4.  Copie el ejemplo del búfer de entrada a la misma ubicación en el búfer de retraso desde el que se recuperó el último ejemplo de retraso.
5.  Mueva el puntero de búfer de retraso hacia delante al siguiente ejemplo. Si el puntero se desplaza más allá del final del búfer, muévalo al encabezado del búfer.
6.  Combine el ejemplo del búfer de entrada con el ejemplo del búfer de retraso.
7.  Copie el resultado en el búfer de salida. A continuación, mueva el puntero del búfer de salida hacia delante a la unidad siguiente para preparar la siguiente iteración del bucle.
8.  Repita el proceso hasta que se procesen todos los ejemplos.

Cuando una muestra de entrada recuperada en el paso 2 se copia en el búfer de retraso en el paso 4, permanece allí hasta que el puntero móvil recorre cada ejemplo en el búfer de retraso y finalmente vuelve a la misma posición. Dado que el tamaño del búfer de retraso está diseñado para que se corresponda con el tiempo de retardo, el tiempo transcurrido entre el ejemplo que se copia en el búfer de retraso y el ejemplo que se recupera una vez más es igual al retraso especificado (más cualquier latencia introducida por el procesamiento real).

Cuando se inicia un flujo, no se generan datos de retraso hasta que ha transcurrido el tiempo de retraso. Por lo tanto, es importante que el búfer de retraso contenga inicialmente el silencio. Si el búfer de retraso contiene datos aleatorios, el usuario oirá el ruido en blanco hasta que el complemento genere suficientes datos de retraso para sobrescribir todo el búfer de retraso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general del ejemplo echo**](echo-sample-overview.md)
</dt> </dl>

 

 




