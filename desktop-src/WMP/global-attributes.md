---
title: Atributos globales (SDK de Windows Media Player)
description: Atributos globales
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Aspectos de Windows Media Player, atributos globales
- máscaras, atributos globales
- referencia de máscaras, atributos globales
- atributos globales
- atributos, globales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104419867"
---
# <a name="global-attributes"></a>Atributos globales

Los atributos globales son atributos que proporcionan un acceso fácil a determinados elementos o objetos del reproductor desde cualquier lugar dentro de una máscara.

El atributo global **Player** es una referencia al objeto [Player](player-object.md) y se utiliza para tener acceso a la funcionalidad principal de Windows Media Player. En el ejemplo siguiente se usa **Player** para comenzar la reproducción de archivos multimedia digitales.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



El atributo global **Theme** es una referencia al elemento [Theme](theme-element.md) . Esta es la manera adecuada para tener acceso a los atributos de **tema** , en lugar de especificar un identificador dentro del elemento de **tema** . En el ejemplo siguiente se usa el **tema** para abrir una nueva vista.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



El atributo de **vista** global es una referencia a la [vista](view-element.md)actual. Se puede utilizar en lugar del identificador especificado dentro de los distintos elementos de **vista** . En el ejemplo siguiente se usa la **vista** para cerrar la vista actual.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



El atributo global **Event** se usa para tener acceso a los atributos de evento de ambiente desde los controladores de eventos. En el ejemplo siguiente se utiliza el **evento** para determinar si se presiona la tecla Alt al hacer clic en un botón.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



El atributo global **playerApplication** es una referencia al objeto [playerApplication](playerapplication-object.md) y lo usan los archivos de máscara proporcionados como interfaces de usuario personalizadas para los controles de reproductor remotos. El control Player solo se puede incrustar en modo remoto en programas de C++ que implementan la interfaz **IWMPRemoteMediaServices** . En el ejemplo siguiente se usa **playerApplication** para cambiar al modo completo del reproductor.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Para obtener más información, consulte [atributos de evento ambiente](ambient-event-attributes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Varios**](miscellaneous.md)
</dt> </dl>

 

 




