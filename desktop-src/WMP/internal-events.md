---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Reproductor de Windows Media máscaras,eventos internos
- máscaras, eventos internos
- events,internal
- escribir código para máscaras,eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8859ed86cb4951509d452b24c108e73d4129e474abf1c0bc2f51487e2d42bd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572525"
---
# <a name="internal-events"></a>Eventos internos

Puede detectar los cambios que se producen en Reproductor de Windows Media cambios en su propia máscara. Estos pueden ser cambios en Reproductor de Windows Media propiedades o métodos de objeto, cambios en los atributos de máscara, y así sucesivamente.

## <a name="windows-media-player-property-changes"></a>Reproductor de Windows Media Cambios de propiedad

Puede procesar los cambios en Reproductor de Windows Media mediante el agente de escucha wmpprop. Debe configurar el agente de escucha como un valor de un atributo. Coloque el valor entre comillas dobles y comience con la palabra "wmpprop" seguida de dos puntos. A continuación, incluya la propiedad que desea escuchar. Cuando cambia la propiedad, el valor del atributo también cambiará. Por ejemplo, para que un valor de elemento deslizante cambie cada vez que cambie el valor del atributo **currentPosition,** escriba lo siguiente:


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **Importante** No use wmpprop en Reproductor de Windows Media métodos. Pueden producirse resultados inesperados.

## <a name="windows-media-player-method-changes"></a>Reproductor de Windows Media Cambios en el método

Puede hacer que la máscara responda a la disponibilidad de métodos en Reproductor de Windows Media mediante wmpenabled y wmpdisabled. Se usan de forma similar al agente de escucha wmpprop, salvo que solo se pueden usar en los métodos del **objeto Control** admitidos por el **método isAvailable.**

Por ejemplo, podría habilitar un botón solo cuando el **método Play** está habilitado, mediante código como este:


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **Importante** No use wmpenabled ni wmpdisabled en Reproductor de Windows Media propiedades. Pueden producirse resultados inesperados.

## <a name="skin-attribute-changes"></a>Cambios en los atributos de máscara

Puede responder a los cambios en los atributos de máscara de una de estas dos maneras, mediante wmpprop o el **\_ evento onchange.**

Puede usar wmpprop para escuchar los cambios en su propia máscara. Por ejemplo, para mostrar el valor slider en un cuadro de texto, podría escribir lo siguiente:


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



Puede usar el evento **\_ onchange** para procesar eventos dentro de un elemento . Debe adjuntar el nombre del atributo del que desea realizar el seguimiento **\_ a onchange**. Por ejemplo, si desea realizar un seguimiento del valor de un cuadro de texto, escribiría:


```C++
value_onchange

```



A continuación, asignaría una JScript que desea ejecutar cuando cambie el valor. Por ejemplo, para responder a un cambio en el valor de un cuadro de texto que se puede usar para ajustar el volumen de Reproductor de Windows Media, escriba lo siguiente dentro del elemento **TEXT** como atributo:


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos**](handling-events.md)
</dt> </dl>

 

 




