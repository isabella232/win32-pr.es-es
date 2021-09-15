---
title: Valores preestablecidos
description: Valores preestablecidos
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- visualizaciones, valores preestablecidos
- visualizaciones personalizadas, valores preestablecidos
- visualizaciones, valor preestablecido de barra
- visualizaciones personalizadas, valor preestablecido de barra
- visualizaciones, valor preestablecido de onda
- visualizaciones personalizadas, valor preestablecido wave
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, valores preestablecidos
- visualizations,GetPresetTitle ( Función)
- visualizaciones personalizadas, función GetPresetTitle
- Función GetPresetTitle
- enumeraciones, valores preestablecidos de visualización
- visualizaciones, enumeraciones
- visualizaciones personalizadas, enumeraciones
- visualizaciones, encabezado de recurso y cadenas
- visualizaciones personalizadas, encabezado de recurso y cadenas
- valores preestablecidos en visualizaciones, valor preestablecido de barra
- valores preestablecidos en visualizaciones, valor preestablecido de onda
- valores preestablecidos en visualizaciones, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359452"
---
# <a name="presets"></a>Valores preestablecidos

Los valores preestablecidos se proporcionan como una manera de tener distintos efectos procedentes de la misma visualización. Por ejemplo, podría crear un efecto de efecto de brillo generado por un bloque de código, pero usar un valor preestablecido para determinar el color del brillo. Los nombres preestablecidos pueden ser Rojo, Verde y Azul.

El asistente define dos valores preestablecidos para el código que genera. Una se denomina Barras y la otra se denomina Onda. El valor preestablecido Barras muestra las barras que muestran la actividad en el espectro de audio y usan los datos de forma de onda. El valor preestablecido Wave muestra una línea de alternar que muestra la potencia de audio de la forma de onda.

Si cambia cualquiera de la información preestablecida, también debe cambiar las siguientes partes del código generado.

## <a name="render-function"></a>Función Render

La **función IWMPEffects::Render** se encuentra en el archivo *projectname*.cpp, donde *projectname* es el nombre del proyecto que eligió cuando ejecutó el asistente.

El código generado en la **función Render** usa una instrucción switch para elegir entre dos valores preestablecidos. El valor preestablecido actual es el que el usuario seleccione en Reproductor de Windows Media. Si desea cambiar qué código se ejecuta para un valor preestablecido determinado o agregar o restar un valor preestablecido, modifique la instrucción switch en consecuencia.

Los dos valores preestablecidos se definen mediante las enumeraciones **\_ PRESET BARS** y PRESET **\_ SCOPE.** La elección del valor preestablecido al que se llamará se define mediante m \_ nPreset.

## <a name="getpresettitle"></a>GetPresetTitle

La **función IWMPEffects::GetPresetTitle** se encuentra en el archivo *projectname*.cpp, donde *projectname* es el nombre del proyecto que eligió cuando ejecutó el asistente.

La **función GetPresetTitle** configura las relaciones entre las enumeraciones preestablecidas y los recursos de cadena. El asistente genera las enumeraciones **PRESET \_ BARS** y **PRESET \_ SCOPE** y usan los recursos de cadena IDS \_ BARSPRESETNAME e IDS \_ SCOPEPRESETNAME.

Debe cambiar las enumeraciones y los recursos de cadena si agrega, resta o cambia valores preestablecidos.

## <a name="preset-enumerations"></a>Enumeraciones preestablecidas

La enumeración preestablecida se define en el archivo *projectname*.h, donde *projectname* es el nombre del proyecto que eligió cuando ejecutó el asistente.

La enumeración define los dos valores preestablecidos actuales y el recuento. Si agrega o resta valores preestablecidos o cambia la enumeración, asegúrese de cambiar esta enumeración para que el recuento y el orden de los valores preestablecidos sean correctos. Esta enumeración se usa para asegurarse de llamar al valor preestablecido correcto en la **función Render.**

## <a name="resource-header"></a>Encabezado de recurso

Debe establecer los recursos para los nombres del valor preestablecido en el archivo de encabezado resource.h. Los valores preestablecidos actuales se definen como:


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Si agrega o resta valores preestablecidos, debe cambiar el encabezado del recurso y los números para ellos.

## <a name="resource-strings"></a>Cadenas de recursos

Los nombres reales de los valores preestablecidos se definen en el archivo de recursos *nombrede* proyecto dll.rc, donde *projectname* es el nombre del proyecto que eligió cuando ejecutó el asistente. Puede editar este archivo a mano o usar el editor de recursos incluido con Microsoft Visual C++.

Los nombres generados son el nombre de la visualización más el valor preestablecido específico. El archivo de recursos para el código generado los definirá como:


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



donde *projectname* es el nombre del proyecto que eligió cuando ejecutó el asistente. Aquí es donde cambiará los nombres reales de los valores preestablecidos y así es como se hará referencia a ellos y se mostrarán mediante Reproductor de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar el código**](implementing-your-code.md)
</dt> </dl>

 

 




