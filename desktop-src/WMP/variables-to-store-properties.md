---
title: Variables para almacenar propiedades
description: Variables para almacenar propiedades
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento DSP de eco, variables para almacenar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268940"
---
# <a name="variables-to-store-properties"></a>Variables para almacenar propiedades

En primer lugar, necesitará una variable para almacenar el tiempo de retraso. El ejemplo predeterminado creado por el Asistente para complementos de Windows Media Player proporciona una variable denominada m \_ fScaleFactor para almacenar el multiplicador de escalado que utiliza para el procesamiento. Este ejemplo ya no necesita esta variable, por lo que puede cambiar su nombre y tipo para almacenar el valor de tiempo de retraso.

1.  Reemplace cada instancia de m \_ fScaleFactor en echo. h y ECHO. cpp por m \_ dwDelayTime.
2.  Cambie el tipo de datos de m \_ fScaleFactor (Now \_ dwDelayTime) de Double a DWORD en echo. h.
3.  En el constructor de CEcho, cambie el valor de tiempo de retraso predeterminado a 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

A continuación, declare dos nuevas variables de miembro para almacenar el porcentaje de la señal del efecto y el porcentaje de la señal de origen que se va a mezclar en el búfer de salida final. El término "húmedo" hace referencia al efecto y el término "seco" hace referencia a la señal de origen. Agregue las declaraciones siguientes a ECHO. h:


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Estos valores se almacenan como representaciones decimales de porcentajes, por lo que se pueden usar fácilmente como factores de escala. Por ejemplo, una combinación de efecto del 50 por ciento y una señal de origen del 50 por ciento se representará como un valor de 0,50 para cada variable. La suma de los valores de m \_ fWetMix y m \_ fDryMix no debe ser superior a 1,0 (100 por ciento). Finalmente, estos valores serán accesibles como propiedades.

Agregue el código siguiente al constructor CEcho para establecer los valores predeterminados en 50 por ciento:


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Eco de propiedades de ejemplo**](echo-sample-properties.md)
</dt> </dl>

 

 




