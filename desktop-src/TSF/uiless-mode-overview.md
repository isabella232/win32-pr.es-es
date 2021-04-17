---
title: Información general del modo UILess
description: Información general del modo UILess
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Text Services Framework (TSF), UILessMode
- TSF (marco de trabajo de servicios de texto), UILessMode
- Aplicaciones habilitadas para TSF, UILessMode
- UILessMode
- Marco de trabajo de servicios de texto (TSF), UIElement de la lista de candidatos
- TSF (marco de trabajo de servicios de texto), UIElement List de Candidate
- Aplicaciones habilitadas para TSF, UIElement de la lista de candidatos
- UIElement de la lista de candidatos
- Marco de trabajo de servicios de texto (TSF), sugerencia de UIElement
- TSF (marco de trabajo de servicios de texto), sugerencia de UIElement
- Aplicaciones habilitadas para TSF, sugerencia de UIElement
- SUGERENCIA de UIElement
- Text Services Framework (TSF), elementos de interfaz de usuario predefinidos
- TSF (marco de trabajo de servicios de texto), elementos de interfaz de usuario predefinidos
- Aplicaciones habilitadas para TSF, elementos de interfaz de usuario predefinidos
- elementos de interfaz de usuario predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7354a88fb28fd0d6bf5f4180ac23359a2117fe7
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104558184"
---
# <a name="uiless-mode-overview"></a>Información general del modo UILess

## <a name="how-to-create-uilessmode"></a>Cómo crear UILessMode

**Crear subproceso sin interfaz de usuario:** La aplicación puede hacer que una interfaz de usuario sea menos subproceso por [**ITfThreadMgrEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) con ITF \_ AE \_ UIELEMENTENABLEDONLY. Cuando ThreadMgr se activa con esta marca, solo se activan en el subproceso las sugerencias que pueden controlar su elemento de la interfaz de usuario. La aplicación debe implementar la interfaz [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) y aconsejar la interfaz en el administrador de subprocesos. Se llama a [**ITfUIElementSink:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) cuando la sugerencia muestra su interfaz de usuario. La aplicación puede devolver **true** en el parámetro pbShow para permitir que TIP muestre la interfaz de usuario original de tip cuando la aplicación no desea dibujar. Si la aplicación no permite la interfaz de usuario de la sugerencia, puede devolver **false** en pbShow (vea los diagramas siguientes). La aplicación puede dibujar la interfaz de usuario por sí misma obteniendo cierta información *del parámetro de* el parámetro de la interfaz de usuario. Podría ser la lista de candidatos, el elemento de la barra de idioma o la interfaz de usuario personalizada de TIP. La aplicación puede conocer el tipo de interfaz de usuario de QIing [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) . Cuando se cambia la interfaz de usuario, se llama a [**ITfUIElementSink:: UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) . La aplicación puede comparar el GUID de la >GetGUID () para saber si el elemento está dibujado actualmente por la aplicación.

**Sugerencias para la interfaz de usuario sin tener en cuenta:** SUGERENCIA debe admitir el modo menos de la interfaz de usuario si desea ejecutarse en la aplicación que no desea permitir la interfaz de usuario de la sugerencia, como aplicación de juego o aplicaciones de pantalla completa. Para que la interfaz de usuario sea menos consciente, la sugerencia debe implementar la interfaz [**ITfTextInputProcessorEx**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) . Si no se implementa esta interfaz, la sugerencia no se activará en el subproceso de la interfaz de usuario menos el modo. Además, la sugerencia debe llamar a [**ITFUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) antes de mostrar una interfaz de usuario visible en la pantalla. Este método realiza una llamada a [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) para notificar a la aplicación. Y la aplicación decidirá si puede mostrarse o no. Cuando TIP llama a BeginUIElement (), la sugerencia debe tener la interfaz [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) para la interfaz de usuario correspondiente. La aplicación QI la interfaz para obtener otra interfaz específica de la interfaz de usuario para recuperar más información para dibujar la interfaz de usuario. System predefine [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) y [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) para tip. Cuando la sugerencia desea mostrar la lista de candidatos en el subproceso de la interfaz de usuario menos el modo, TIP debe crear una instancia de la interfaz **ITfCandidateListUIElement** y llamar a **ITFUIElementMgr:: BeginUIElement**. Cuando se llama a [**ITfTextInputProcessorEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) , TIP ya sabe que el subproceso es una interfaz de usuario menos que puede eliminar la interfaz de usuario personalizada adicional. Sin embargo, por supuesto, puede implementar su propia interfaz que se puede QIed desde e intentar realizar una notificación. Por lo tanto, la sugerencia y las **ITfUIElement** de la variable pueden tener una negociación para la interfaz de usuario personalizada de la sugerencia.

## <a name="uielement-supporting-tip"></a>SUGERENCIA compatible con UIElement

La sugerencia que admite el UIElement debe estar clasificada por el GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. La sugerencia en GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED debe usar [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) para mostrar cualquier interfaz de usuario para que la aplicación pueda controlar la visibilidad de la interfaz de usuario.

**Mostrar u ocultar estado de UIElement:** Mostrar u ocultar el estado que indica el método [**ITfUIElement:: show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) o [**ITfUIElement:: IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) es el estado visible real. No está relacionado con la disponibilidad de UIElement. UIElement siempre debe estar disponible cuando el estado de la presentación existe. El estado de la presentación es controlable desde la aplicación. La aplicación puede pasar repentinamente al modo UILess y empezar a dibujar una interfaz de usuario por sí misma, llamando a **ITfUIElement:: show** con **false** para ocultar toda la interfaz de usuario de la sugerencia. A continuación, la sugerencia puede tomar una de algunas opciones. 1) la sugerencia puede trasladar el UIElement al estado de ocultación y comenzar a generar UpdateUIElement. 2) la sugerencia puede finalizar UIElement ya que el elemento de la interfaz de usuario no admite el estado de ocultación y la sugerencia llama a EndUIElement () para finalizarlo.

## <a name="predefined-ui-elements"></a>Elementos de interfaz de usuario predefinidos

**La lista de candidatos:** La lista de candidatos es uno de los principales elementos de la interfaz de usuario para la entrada EA. Este elemento de la interfaz de usuario proporciona la lista de candidatos y el número correspondiente de las cadenas candidatas para el dibujo.

**Ventana de información de lectura** La ventana de información de lectura es común para la entrada de teclado en chino. Tiene la fase que no se puede insertar en el documento como la cadena de composición. Algunos procesadores de entrada en chino abren una pequeña ventana de información de lectura que muestra la información de lectura, fonética o de escritura.

## <a name="the-flow-chart-of-uilessmode"></a>El gráfico de flujo de UILessMode

![Diagrama que muestra el gráfico de flujo U I LessMode.](images/tsf-uilessmode-ovw1.gif)

Una vez que la sugerencia recibe **true** en \* pbShown por [**ITfUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement), la sugerencia no tiene que llamar a UpdateUIElement para el UIElement. Pero TIP debe llamar a EndUIElement () para que [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) y la aplicación puedan realizar el seguimiento del estado de UIElement. TIP debe llamar a UpdateUIElement () después de que BeginUIElement () devuelva **false** en \* pbShow. La aplicación que desea dibujar la interfaz de usuario no comprueba el contenido de BeginUIElement (), simplemente devuelve el estado de la presentación en BeginUIElement () y comienza a comprobar el contenido en UpdateUIElement (). Por ejemplo, la marca de actualización del UIElement de la lista de candidatos tiene todos los bits en la primera UpdateUIElement (). Esto significa que el contenido de UIElement no tiene que estar listo en BeginUIElement ().

![Diagrama que muestra cuando se llama a ' ITUIElementMgr:: BeginUIElement () ' y ' BeginUIElement of UIElementSink ' de la aplicación.](images/tsf-uilessmode-ovw2.gif)![Diagrama que muestra la aplicación devuelve FALSE en * pbShow.](images/tsf-uilessmode-ovw3.gif)![diagrama de flujo de uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>UIElement de la lista de candidatos

**Acerca de PageIndex:** La aplicación que dibuja la lista de candidatos calculará el número de cadenas por página cuando se cambie el contenido de la lista ( \_ \_ se establece TF CLUIE String). No es conveniente cambiar el índice de la página mientras que la lista de candidatos está disponible para el modo UILess. Esto significa que la lista de candidatos de la sugerencia debe comportarse en lugar de desplazarse cuando la selección se mueve a la página siguiente. Si el desplazamiento se produce cuando se mueve la selección, se cambia el índice de la página y la aplicación necesita volver a calcular el índice de la página. Es posible que el resultado no sea el esperado por la sugerencia.

**Ninguna selección:** [**ITfCandidateListUIElement:: getSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) devuelve S \_ false, si la lista de candidatos no tiene una selección. El valor devuelto del primer parámetro no es válido.

 

 




