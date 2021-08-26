---
title: Barra de desplazamiento plano
description: Esta sección contiene información sobre los elementos de programación utilizados para controlar las barras de desplazamiento planas.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466602"
---
# <a name="flat-scroll-bar"></a>Barra de desplazamiento plano

Esta sección contiene información sobre los elementos de programación utilizados para controlar las barras de desplazamiento planas.

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de desplazamiento plano](flat-scroll-bars.md) | Microsoft Internet Explorer 4.0 introdujo una nueva tecnología visual denominada barras de desplazamiento plano. Funcionalmente, las barras de desplazamiento planos se comportan igual que las barras de desplazamiento estándar. La diferencia es que puede personalizar su apariencia en mayor medida que las barras de desplazamiento estándar.<br/> |



 

### <a name="functions"></a>Functions




| Tema | Contenido | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Habilita o deshabilita uno o ambos botones de dirección de la barra de desplazamiento plano. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>función EnableScrollBar</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Obtiene la información de una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Obtiene la posición del control en una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Obtiene las propiedades de una barra de desplazamiento plana. Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Obtiene las propiedades de una barra de desplazamiento plana. Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana.<blockquote>[!Note]<br />Esto es idéntico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Obtiene el intervalo de desplazamiento de una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Establece la información de una barra de desplazamiento plano. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>función SetScrollInfo</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Establece la posición actual del control en una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>función SetScrollPos</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Establece las propiedades de una barra de desplazamiento plana. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Establece el intervalo de desplazamiento de una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Muestra u oculta una barra de desplazamiento plana. Si no se inicializan barras de desplazamiento planas para la ventana, esta función llama a la <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>función ShowScrollBar</strong></a> estándar. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | Inicializa barras de desplazamiento planas para una ventana determinada. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | Desinicializa las barras de desplazamiento planas de una ventana determinada. La ventana especificada se revertirá a las barras de desplazamiento estándar. <br /> | 




 

 

 





