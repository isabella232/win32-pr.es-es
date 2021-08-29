---
title: Variables para almacenar propiedades
description: Variables para almacenar propiedades
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Reproductor de Windows Media complementos, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, propiedades de ejemplo de eco
- Complementos DE DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento DSP de eco, variables para almacenar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8a1ca4f7e83fe18dabafca6015059dc8ed01deb54ad9f9bc63515ded45c076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001355"
---
# <a name="variables-to-store-properties"></a>Variables para almacenar propiedades

En primer lugar, necesitará una variable para almacenar el tiempo de retraso. El ejemplo predeterminado creado por Reproductor de Windows Media Asistente para complementos proporciona una variable denominada m fScaleFactor para almacenar el multiplicador de escalado que \_ usa para el procesamiento. Este ejemplo ya no necesita esta variable, por lo que puede cambiar su nombre y tipo para almacenar el valor de tiempo de retraso.

1.  Reemplace cada instancia de m \_ fScaleFactor en Echo.h y Echo.cpp por m \_ dwDelayTime.
2.  Cambie el tipo de datos de m \_ fScaleFactor (ahora m \_ dwDelayTime) de double a DWORD en Echo.h.
3.  En el constructor de CEcho, cambie el valor de tiempo de retraso predeterminado a 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

A continuación, declare dos nuevas variables miembro para almacenar el porcentaje de señal de efecto y el porcentaje de señal de origen que se va a mezclar en el búfer de salida final. El término "efectos" hace referencia al efecto y el término "dry" hace referencia a la señal de origen. Agregue las siguientes declaraciones a Echo.h:


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Estos valores se almacenan como representaciones decimales de porcentajes para que se puedan usar fácilmente como factores de escala. Por ejemplo, una mezcla de efecto del 50 % y señal de origen del 50 % se representaría como un valor de 0,50 para cada variable. La suma de los valores de m fWetMix y m fDryMix no debe ser superior a \_ \_ 1,0 (100 por ciento). Finalmente, estos valores serán accesibles como propiedades.

Agregue el código siguiente al constructor CEcho para establecer los valores predeterminados en 50 por ciento cada uno:


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades de ejemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




