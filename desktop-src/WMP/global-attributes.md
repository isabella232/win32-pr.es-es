---
title: Atributos globales (Reproductor de Windows Media SDK)
description: Atributos globales
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Reproductor de Windows Media máscaras,atributos globales
- máscaras, atributos globales
- referencia de máscaras, atributos globales
- atributos globales
- attributes,global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648085"
---
# <a name="global-attributes"></a>Atributos globales

Los atributos globales son atributos que proporcionan un acceso sencillo a determinados elementos u objetos del reproductor desde cualquier lugar dentro de una máscara.

El **atributo** global player es una referencia al [objeto Player](player-object.md) y se usa para acceder a la funcionalidad principal de Reproductor de Windows Media. En el ejemplo siguiente se usa **el reproductor** para iniciar la reproducción multimedia digital.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



El **atributo** global de tema es una referencia al [elemento THEME.](theme-element.md) Esta es la manera adecuada de acceder a **los atributos THEME,** en lugar de especificar un identificador dentro del **elemento THEME.** En el ejemplo siguiente se **usa el** tema para abrir una nueva vista.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



El **atributo** global de vista es una referencia a la [vista actual.](view-element.md) Se puede usar en lugar del identificador especificado dentro de los **distintos elementos VIEW.** En el ejemplo siguiente se **usa view** para cerrar la vista actual.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



El **atributo** global de evento se usa para tener acceso a los atributos de eventos de ambiente desde los controladores de eventos. En el ejemplo siguiente se **usa el** evento para determinar si se presiona la tecla ALT cuando se hace clic en un botón.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



El atributo global **playerApplication** es una referencia al objeto [PlayerApplication](playerapplication-object.md) y lo usan los archivos de máscara proporcionados como interfaces de usuario personalizadas para los controles player remotos. El control Player solo se puede incrustar en modo remoto en programas de C++ que implementan la **interfaz IWMPRemoteMediaServices.** En el ejemplo siguiente se **usa playerApplication** para cambiar al modo completo del reproductor.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Para obtener más información, vea [Atributos de evento ambiente](ambient-event-attributes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Varios**](miscellaneous.md)
</dt> </dl>

 

 




