---
title: Barra de idioma (servicios de texto)
description: Barra de idioma
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Marco de trabajo de servicios de texto (TSF), barra de idioma
- TSF (marco de trabajo de servicios de texto), barra de idioma
- servicios de texto, barra de idioma
- barra de idioma
- Text Services Framework (TSF), botones
- TSF (marco de trabajo de servicios de texto), botones
- servicios de texto, botones
- Text Services Framework (TSF), menús
- TSF (marco de trabajo de servicios de texto), menús
- servicios de texto, menús
- estilos de botón
- botones de menú
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41d64a488406f6eefcff5fef6c11093af00bc5b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421860"
---
# <a name="language-bar-text-services"></a>Barra de idioma (servicios de texto)

## <a name="implementing-the-language-bar-object"></a>Implementar el objeto de barra de idioma

Para permitir agregar un elemento a la barra de idioma, un servicio de texto debe implementar un objeto que admita la interfaz [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) y uno de los elementos de control [ITfLangBarItem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) . Cuando se instala el elemento, la barra de idioma instala un receptor de [ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) llamando a [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) del elemento con IID \_ ITfLangBarItemSink. El elemento usa la interfaz **ITfLangBarItemSink** para notificar los cambios en la barra de idioma, por ejemplo, cuando el elemento se oculta, se muestra, se habilita o se deshabilita.

Se pueden instalar cuatro tipos de elementos de barra de idioma y cada una de las interfaces necesarias se crea a partir de **ITfLangBarItem**. A continuación se muestran los posibles elementos de control **ITfLangBarItem** .



|               |                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botón        | Un botón de barra de idioma funciona como un botón de comando, un control de alternancia o un menú en la barra de idioma. El objeto debe admitir la interfaz ITfLangBarItemButton.                   |
| LDM       | Un globo de barra de idioma funciona como una notificación emergente en la barra de idioma. El objeto debe admitir la interfaz ITfLangBarItemBalloon.                                       |
| Bitmap        | Un mapa de bits de la barra de idioma funciona como un elemento estático en la barra de idioma que muestra un mapa de bits. El objeto debe admitir la interfaz ITfLangBarItemBitmap.                       |
| Botón de mapa de bits | Un botón de mapa de bits de la barra de idioma funciona como un elemento de botón en la barra de idioma que muestra texto y un mapa de bits. El objeto debe admitir la interfaz ITfLangBarItemBitmapButton. |



 

## <a name="button-styles"></a>Estilos de botón

Un elemento Button puede funcionar como cualquiera de los siguientes. La función del elemento de botón viene determinada por las marcas establecidas en el miembro **dwStyle** de la estructura [TF \_ LANGBARITEMINFO](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) en el método [ITfLangBarItem:: GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) .



|               |                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botón        | El botón funciona como un botón de comando estándar. Este estilo de botón se identifica mediante el estilo de botón del botón de la función de TF \_ LBI \_ \_ \_ . Se llama a ITfLangBarItemButton:: OnClick cuando se hace clic en el elemento. No se usan ITfLangBarItemButton:: InitMenu y ITfLangBarItemButton:: OnMenuSelect.                                                                                                   |
| Botón de alternancia | El botón funciona como un control de alternancia que puede mantener un estado de clic, similar a una casilla. Este estilo de botón se identifica mediante el estilo de alternancia de tipo de comando TF \_ LBI \_ \_ \_ . Se llama a ITfLangBarItemButton:: OnClick cuando se hace clic en el elemento. No se usan ITfLangBarItemButton:: InitMenu y ITfLangBarItemButton:: OnMenuSelect.                                                  |
| Menú          | El botón funciona como un menú desplegable. Este estilo de botón se identifica mediante el \_ estilo de menú de TF LBI \_ style \_ BTN \_ . Se llama a ITfLangBarItemButton:: InitMenu cuando se hace clic en el botón. Cuando el usuario selecciona un elemento en el menú, la barra de idioma llama a ITfLangBarItemButton:: OnMenuSelect con el identificador del elemento de menú seleccionado. ITfLangBarItemButton:: unclick no se utiliza. |



 

## <a name="implementing-a-menu-button"></a>Implementar un botón de menú

Cuando el usuario hace clic en un botón de menú, la barra de idioma llama a [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu). El elemento agrega elementos al menú mediante la interfaz [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) pasada a InitMenu.

Para agregar un submenú al menú, llame a [ITfMenu:: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) con el \_ \_ submenú TF LBMENUF. Cuando esto se hace, se devuelve un nuevo objeto **ITfMenu** que representa el submenú en el parámetro *ppMenu* de AddMenuItem. Este nuevo objeto de menú se usa para agregar elementos al submenú.

Cuando el usuario selecciona un elemento en el menú, la barra de idioma llama a [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) con el identificador del elemento de menú seleccionado.

## <a name="adding-items-to-the-language-bar"></a>Agregar elementos a la barra de idioma

Un servicio de texto debe agregar sus elementos a la barra de idioma cuando se llama a su método [ITfTextInputProcessor:: Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) y quitarlos cuando se llama a [ITfTextInputProcessor::D eactivate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) .

Para agregar un elemento a la barra de idioma, el servicio de texto obtiene una interfaz [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) llamando a ITfThreadMgr:: QUERYINTERFACE con IID \_ ITfLangBarItemMgr. Después, el servicio de texto llama a [ITfLangBarItemMgr:: AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) con el puntero al objeto de elemento de barra de idioma.

El servicio de texto debe quitar el elemento cuando se desactiva. El servicio de texto usa la misma interfaz **ITfLangBarItemMgr** que se usa para agregar los elementos u obtener otra instancia de la interfaz. Después, el servicio de texto llama a [ITfLangBarItemMgr:: RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) con el puntero de interfaz del elemento que se va a quitar.

## <a name="extending-system-language-bar-items"></a>Extender elementos de la barra de idioma del sistema

TSF proporciona la capacidad de agregar elementos de menú a los menús de barra de idioma existentes. Esto permite a un servicio de texto agregar elementos al menú de otro servicio de texto sin tener que agregar un botón independiente a la barra de herramientas. Esto también permite organizar los elementos de menú en grupos lógicos. Por ejemplo, un servicio de texto que proporciona características adicionales al servicio de texto de voz estándar puede agregar elementos al menú servicio de texto de voz en lugar de agregar su propio botón de menú de nivel superior.

Un servicio de texto proporciona una extensión de menú de barra de idioma implementando un objeto que admite la interfaz [ITfSystemLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) . Esta interfaz funciona exactamente igual que la interfaz [ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) para un botón de menú. Cuando se muestra el menú, el servicio de texto que se extiende llama a [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu). La extensión agrega elementos al menú mediante la interfaz [ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) pasada a **InitMenu**. Cuando el usuario selecciona un elemento agregado por la extensión, el servicio de texto que se extiende llama a [ITfSystemLangBarItemSink:: OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) con el identificador del elemento de menú seleccionado.

Para instalar una extensión de menú de la barra de idioma, el servicio de texto completa los pasos siguientes.

1.  Obtenga la interfaz **ITfLangBarItem** para el elemento que se va a extender llamando a [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) con el **GUID** para el elemento que se va a extender.
2.  Obtenga la interfaz **ITfSource** para el elemento que se va a extender llamando a ITfLangBarItem:: QUERYINTERFACE con IID \_ ITfSource.
3.  Llame a [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfSystemLangBarItemSink y el puntero al objeto **ITfSystemLangBarItemSink** . Si ITfSource:: AdviseSink produce un error, el servicio de texto no admite extensiones de menú.

[ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource:: AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Extensiones de menú de la barra de idioma compatible

Un servicio de texto puede permitir que otros servicios de texto agreguen elementos a sus menús de barra de idioma, tal como se mostró anteriormente. Servicio de texto que debe publicar su GUID para que el elemento se pueda obtener llamando a [ITfLangBarItemMgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem).

Para admitir las extensiones de menú, el servicio de texto debe admitir la interfaz [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) . Los pasos siguientes habilitan la compatibilidad con una o más extensiones de menú.

1.  Cuando se llama a [ITfSource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfSystemLangBarItemSink, el servicio de texto debe almacenar la interfaz **ITfSystemLangBarItemSink** y devolver un valor de cookie que identificará la extensión.
2.  Cuando se llama a [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) , el servicio de texto llama al método [ITfSystemLangBarItemSink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) de la extensión. El servicio de texto debe implementar una manera de identificar los elementos de menú agregados por la extensión en lugar de los elementos agregados por el propio servicio de texto.
3.  Cuando se llama a [ITfLangBarItemButton:: OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) con un identificador de elemento de menú que pertenece a una extensión, el servicio de texto llama al método **ITfSystemLangBarItemSink:: OnMenuSelect** de las extensiones.
4.  Cuando se llama a [ITfSource:: UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) con la cookie adecuada, el servicio de texto quita la extensión de menú.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo configurar el marco de trabajo de servicios de texto](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de idioma (aplicaciones)](language-bar-app.md)
</dt> </dl>

 

 
