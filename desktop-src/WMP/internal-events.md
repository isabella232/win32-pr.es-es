---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Aspectos de Windows Media Player, eventos internos
- máscaras, eventos internos
- eventos, internos
- escribir código para máscaras, eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994012"
---
# <a name="internal-events"></a>Eventos internos

Puede detectar los cambios que se producen en Windows Media Player o los cambios en su propia máscara. Estos pueden ser cambios en las propiedades o los métodos de los objetos de Windows Media Player, los cambios en los atributos de máscara, etc.

## <a name="windows-media-player-property-changes"></a>Cambios en las propiedades de Media Player de Windows

Puede procesar los cambios en Windows Media Player mediante el agente de escucha wmpprop. Debe configurar el agente de escucha como un valor de un atributo. Ponga el valor entre comillas dobles y empiece con la palabra "wmpprop" seguida de dos puntos. Después, incluya la propiedad que desea escuchar. Cuando cambie la propiedad, también cambiará el valor del atributo. Por ejemplo, para cambiar el valor de un elemento Slider cuando cambie el valor del atributo **currentPosition** , escriba lo siguiente:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** No use wmpprop en métodos de Media Player de Windows. Pueden producirse resultados inesperados.

## <a name="windows-media-player-method-changes"></a>Cambios del método de Windows Media Player

Puede hacer que la máscara responda a la disponibilidad de métodos en Windows Media Player mediante wmpenabled y wmpdisabled. Se usan de forma similar al agente de escucha wmpprop, salvo que solo se pueden usar en métodos del objeto de **control** que son compatibles con el método **isavailable** .

Por ejemplo, puede habilitar un botón solo cuando el método **Play** está habilitado, mediante código como el siguiente:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** No use wmpenabled o wmpdisabled en las propiedades de Media Player de Windows. Pueden producirse resultados inesperados.

## <a name="skin-attribute-changes"></a>Cambios en los atributos de máscara

Puede responder a los cambios en los atributos de máscara de una de las dos maneras siguientes: mediante wmpprop o el evento **\_ onchange** .

Puede usar wmpprop para escuchar los cambios en su propia máscara. Por ejemplo, para mostrar el valor del control deslizante en un cuadro de texto, puede escribir lo siguiente:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Puede usar el evento **\_ onchange** para procesar eventos dentro de un elemento. Debe adjuntar el nombre del atributo del que desea realizar un seguimiento a **\_ onchange**. Por ejemplo, si desea realizar un seguimiento del valor de un cuadro de texto, debe escribir:


```C++
value_onchange

```



A continuación, asignaría una cadena de JScript que desea ejecutar cuando el valor cambie. Por ejemplo, para responder a un cambio en el valor de un cuadro de texto que se puede usar para ajustar el volumen de Windows Media Player, escriba lo siguiente en el elemento de **texto** como atributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controlar eventos**](handling-events.md)
</dt> </dl>

 

 




