---
title: Información general sobre el modo sin interfaz de usuario
description: Información general sobre el modo sin interfaz de usuario
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Text Services Framework (TSF),UILessMode
- TSF (Text Services Framework),UILessMode
- Aplicaciones habilitadas para TSF,UILessMode
- UILessMode
- Text Services Framework (TSF),candidate list UIElement
- TSF (Text Services Framework),candidate list UIElement
- Aplicaciones habilitadas para TSF, lista de candidatos UIElement
- candidate list UIElement
- Text Services Framework (TSF),SUGERENCIA DE UIElement
- TSF (Text Services Framework),UIElement TIP
- Aplicaciones habilitadas para TSF, SUGERENCIA DE UIElement
- SUGERENCIA DE UIElement
- Text Services Framework (TSF), elementos predefinidos de la interfaz de usuario
- TSF (Text Services Framework), elementos predefinidos de la interfaz de usuario
- Aplicaciones habilitadas para TSF, elementos predefinidos de la interfaz de usuario
- elementos predefinidos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdac8e43cc8342c50a6d232b801af0c65315fd407b9f413f2b5fdcb7074282fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949868"
---
# <a name="uiless-mode-overview"></a>Información general sobre el modo sin interfaz de usuario

## <a name="how-to-create-uilessmode"></a>Cómo crear UILessMode

**Crear un subproceso sin interfaz de usuario:** La aplicación puede hacer que una interfaz de usuario sea menos subproceso [**por ITfThreadMgrEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) con ITF \_ AE \_ UIELEMENTENABLEDONLY. Cuando ThreadMgr se activa con esta marca, solo se activan en el subproceso las TIP que pueden controlar su elemento de interfaz de usuario. La aplicación debe implementar la [**interfaz ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) y aconsejar a la interfaz en el administrador de subprocesos. [**Se llama a ITfUIElementSink::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) cuando TIP muestra su interfaz de usuario. La aplicación puede devolver **TRUE en** pbShow param para permitir que TIP muestre la interfaz de usuario original de TIP cuando la aplicación no desea dibujar. Si la aplicación no permite la interfaz de usuario de TIP, puede devolver **FALSE** en pbShow (consulte los diagramas siguientes). La aplicación puede dibujar la interfaz de usuario por sí misma obteniendo información del *param pElement.* Podría ser la lista de candidatos, el elemento de la barra de idioma o la interfaz de usuario personalizada de TIP. La aplicación puede conocer el tipo de interfaz de usuario mediante la interfaz [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) de QIing. Cuando se cambia la interfaz de usuario, [**se llama a ITfUIElementSink::UpdateUIElement.**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) La aplicación puede comparar el GUID de pElement->GetGUID() para saber si la aplicación dibuja actualmente el elemento.

**Hacer sugerencias para la interfaz de usuario sin tener en cuenta:** TIP debe admitir el modo menos de interfaz de usuario si quiere ejecutarse en la aplicación que no quiere permitir la interfaz de usuario de TIP, como aplicaciones de juegos o aplicaciones de pantalla completa. Para que la interfaz de usuario sea menos consciente, TIP debe implementar [**la interfaz ITfTextInputProcessorEx.**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) Si no se implementa esta interfaz, TIP no se activará en el subproceso de modo menos de la interfaz de usuario. Además, TIP debe llamar a [**ITFUIElementMgr::BeginUIElement antes**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) de mostrar una interfaz de usuario visible en la pantalla. Este método realiza una llamada a [**ITfUIElementSink para**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) notificar a la aplicación. Y la aplicación decidirá si se puede mostrar o no. Cuando TIP llama a BeginUIElement(), TIP debe tener la [**interfaz ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) para la interfaz de usuario correspondiente. La aplicación hará que la interfaz obtenga otra interfaz específica de la interfaz de usuario para recuperar más información para dibujar la interfaz de usuario. El sistema predefine [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) [**e ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) para TIP. Cuando TIP quiere mostrar la lista de candidatos en el subproceso de modo menos de la interfaz de usuario, TIP debe crear una instancia de la interfaz **ITfCandidateListUIElement** y llamar a **ITFUIElementMgr::BeginUIElement**. Cuando se llama a [**ITfTextInputProcessorEx::ActivateEx,**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) TIP ya sabe que el subproceso es la interfaz de usuario menos, por lo que puede eliminar la interfaz de usuario personalizada adicional. Sin embargo, por supuesto, puede implementar su propia interfaz desde la que se puede realizar una IA e intentar realizar una notificación. Por lo tanto, TIP y la aplicación **ITfUIElement** pueden tener una negociación para la interfaz de usuario personalizada de TIP.

## <a name="uielement-supporting-tip"></a>SUGERENCIA compatible con UIElement

La SUGERENCIA que admite UIElement debe clasificarse por GUID \_ \_ TIPCAP \_ UIELEMENTENABLED. La SUGERENCIA en GUID \_ \_ TFCAT TIPCAP UIELEMENTENABLED debe usar \_ [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) para mostrar cualquier interfaz de usuario para que la aplicación pueda controlar la visibilidad de la interfaz de usuario.

**Mostrar u ocultar el estado de UIElement:** Mostrar u ocultar el estado indicado por el método [**ITfUIElement::Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) o [**ITfUIElement::IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) es el estado visible real. No está relacionado con la disponibilidad de UIElement. UIElement debe estar siempre disponible cuando existe el estado de presentación. El estado de la presentación se puede controlar desde la aplicación. La aplicación puede pasar repentinamente al modo sin interfaz de usuario y empezar a dibujar alguna interfaz de usuario por sí misma, llamando a **ITfUIElement::Show** con **FALSE** para ocultar toda la interfaz de usuario de TIP. A continuación, TIP puede tomar una de algunas opciones. 1) TIP puede mover UIElement al estado Ocultar y empezar a generar UpdateUIElement. 2) TIP puede finalizar UIElement, ya que el elemento de interfaz de usuario no admite ocultar el estado y Tip llama a EndUIElement() para finalizarlo.

## <a name="predefined-ui-elements"></a>Elementos predefinidos de la interfaz de usuario

**Lista de candidatos:** La lista de candidatos es uno de los elementos principales de la interfaz de usuario para la entrada de EA. Este elemento de la interfaz de usuario proporciona la lista de candidatos y el número correspondiente de las cadenas candidatas para dibujar.

**Ventana de información de lectura** La ventana de información de lectura es común para la entrada de teclado chino. Tiene la fase que no se puede insertar en el documento como la cadena de composición. Algunos procesadores de entrada chino abren una pequeña ventana de información de lectura que muestra la información de lectura, fonética o de escritura.

## <a name="the-flow-chart-of-uilessmode"></a>Gráfico de flujo de UILessMode

![Diagrama que muestra el gráfico de flujo LessMode de U I.](images/tsf-uilessmode-ovw1.gif)

Una vez que TIP recibe **TRUE** en \* pbShown de [**ITfUIElementMgr::BeginUIElement,**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement)tip no tiene que llamar a UpdateUIElement para UIElement. Pero TIP debe llamar a EndUIElement() para que [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) y la aplicación puedan realizar un seguimiento del estado de UIElement. TIP debe llamar a UpdateUIElement() después de que BeginUIElement() devuelva **FALSE** en \* pbShow. La aplicación que quiere dibujar la interfaz de usuario no comprueba el contenido de BeginUIElement(), simplemente devuelve el estado de presentación en BeginUIElement() y comienza a comprobar el contenido en UpdateUIElement(). Por ejemplo, la marca de actualización de la lista candidata UIElement tiene todos los bits en el primer Elemento UpdateUIElement(). Esto significa que el contenido de UIElement no tiene que estar listo en BeginUIElement().

![Diagrama en el que se muestra cuándo la IP llama a 'ITUIElementMgr::BeginUIElement()' y 'BeginUIElement del UIElementSink de la aplicación'.](images/tsf-uilessmode-ovw2.gif)![Diagrama que muestra que la aplicación devuelve FALSE en *pbShow.](images/tsf-uilessmode-ovw3.gif)![gráfico de flujo uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>UiElement de la lista de candidatos

**Acerca de PageIndex:** La aplicación que dibuja la lista de candidatos calculará el número de cadenas por página cuando se cambie el contenido de la lista (se establece TF \_ CLUIE \_ STRING). No es bueno cambiar el índice de página mientras la lista de candidatos esté disponible para el modo sin interfaz de usuario. Esto significa que la lista de candidatos de TIP debe comportar la paginación en lugar de desplazarse cuando la selección se mueve a la página siguiente. Si el desplazamiento se produce en los movimientos de selección, se cambia el índice de la página y la aplicación debe volver a calcular el índice de la página. Tip puede no esperar el resultado.

**Ninguna selección:** [**ITfCandidateListUIElement::GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) devuelve S FALSE, si la lista \_ de candidatos no tiene una selección. El valor devuelto del primer parámetro no es válido.

 

 




