---
title: Valores preestablecidos
description: Valores preestablecidos
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- visualizaciones, valores preestablecidos
- visualizaciones personalizadas, valores preestablecidos
- visualizaciones, valores preestablecidos de barra
- visualizaciones personalizadas, valores preestablecidos de barra
- visualizaciones, valores preestablecidos de onda
- visualizaciones personalizadas, valores preestablecidos de onda
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, valores preestablecidos
- visualizaciones, función GetPresetTitle
- visualizaciones personalizadas, función GetPresetTitle
- GetPresetTitle función)
- enumeraciones, valores preestablecidos de visualización
- visualizaciones, enumeraciones
- visualizaciones personalizadas, enumeraciones
- visualizaciones, encabezado y cadenas de recursos
- visualizaciones personalizadas, encabezado y cadenas de recursos
- valores preestablecidos en visualizaciones, barra preestablecida
- valores preestablecidos en visualizaciones, presintonías de onda
- valores preestablecidos en visualizaciones, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268627"
---
# <a name="presets"></a>Valores preestablecidos

Los valores preestablecidos se proporcionan como una manera de tener distintos efectos procedentes de la misma visualización. Por ejemplo, podría crear un efecto de resplandor generado por un bloque de código, pero usar un valor preestablecido para determinar el color del resplandor. Los nombres preestablecidos pueden ser rojo, verde y azul.

El asistente define dos valores preestablecidos para el código que genera. Una se denomina barras y la otra se denomina Wave. El valor preestablecido de barras muestra las barras que muestran la actividad en el espectro de audio y utilizan los datos de la onda de onda. El valor preestablecido de onda muestra una línea ondulada que muestra la potencia de audio de la onda.

Si cambia la información preestablecida, también debe cambiar las siguientes partes del código generado.

## <a name="render-function"></a>Render (función)

La función **IWMPEffects:: Render** está en el archivo *projectname*. cpp, donde *projectname* es el nombre del proyecto que eligió al ejecutar el asistente.

El código generado en la función **Render** usa una instrucción switch para elegir entre dos valores preestablecidos. El valor preestablecido actual es lo que el usuario selecciona en Windows Media Player. Si desea cambiar el código que se ejecuta para un valor preestablecido determinado o agregar o restar un valor preestablecido, modifique la instrucción switch en consecuencia.

Los dos valores preestablecidos se definen mediante las **\_ barras preestablecidas** y las enumeraciones de **\_ ámbito preestablecido** . La elección del valor preestablecido que se llamará se define en m \_ nPreset.

## <a name="getpresettitle"></a>GetPresetTitle

La función **IWMPEffects:: GetPresetTitle** está en el archivo *projectname*. cpp, donde *projectname* es el nombre del proyecto que eligió al ejecutar el asistente.

La función **GetPresetTitle** configura las relaciones entre las enumeraciones preestablecidas y los recursos de cadena. El asistente genera **las \_ barras preestablecidas** y el **\_ ámbito de valores** PREestablecidos que usan los identificadores de los recursos de cadena \_ BARSPRESETNAME e IDS \_ SCOPEPRESETNAME.

Debe cambiar las enumeraciones y los recursos de cadena si agrega, resta o cambia valores preestablecidos.

## <a name="preset-enumerations"></a>Enumeraciones preestablecidas

La enumeración preestablecida se define en el archivo *projectname*. h, donde *projectname* es el nombre del proyecto que eligió al ejecutar el asistente.

La enumeración define los dos valores preestablecidos actuales y el recuento. Si agrega o resta valores preestablecidos o cambia la enumeración, asegúrese de cambiar esta enumeración para que el recuento y el orden de los valores preestablecidos sea correcto. Esta enumeración se utiliza para asegurarse de que se llama al valor preestablecido correcto en la función de **representación** .

## <a name="resource-header"></a>Encabezado de recurso

Debe establecer los recursos de los nombres de los valores predeterminados en el archivo de encabezado Resource. h. Los valores preestablecidos actuales se definen como:


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Si agrega o resta valores preestablecidos, debe cambiar el encabezado de recursos y los números correspondientes.

## <a name="resource-strings"></a>Cadenas de recursos

Los nombres reales de los valores preestablecidos se definen en el archivo de recursos *projectname* dll. rc, donde *projectname* es el nombre del proyecto que eligió al ejecutar el asistente. Puede editar este archivo manualmente o usar el editor de recursos incluido con Microsoft Visual C++.

Los nombres generados son el nombre de la visualización más el valor preestablecido específico. El archivo de recursos para el código generado lo definirá como:


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



donde *projectname* es el nombre del nombre del proyecto que eligió al ejecutar el asistente. Aquí es donde cambiará los nombres reales de los valores preestablecidos y así es como se hará referencia a ellos y se mostrarán en Windows Media Player.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar el código**](implementing-your-code.md)
</dt> </dl>

 

 




