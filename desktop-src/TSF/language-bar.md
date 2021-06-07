---
title: Barra de idioma (Text Services)
description: Barra de idioma
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Text Services Framework (TSF),barra de idioma
- TSF (Text Services Framework),barra de idioma
- servicios de texto, barra de idioma
- barra de idioma
- Text Services Framework (TSF),buttons
- TSF (Text Services Framework),buttons
- servicios de texto, botones
- Text Services Framework (TSF),menus
- TSF (Text Services Framework),menus
- servicios de texto, menús
- estilos de botón
- botones de menú
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3c4359c6753f5d96613435f9501036f1d5f317
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524449"
---
# <a name="language-bar-text-services"></a>Barra de idioma (Text Services)

## <a name="implementing-the-language-bar-object"></a>Implementar el objeto de barra de lenguaje

Para admitir la adición de un elemento a la barra de lenguaje, un servicio de texto debe implementar un objeto que admita la interfaz [ITfSource](/windows/desktop/api/msctf/nn-msctf-itfsource) y uno de los elementos de control [ITfLangBarItem.](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) Cuando se instala el elemento, la barra de idioma instala un receptor [ITfLangBarItemSink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) llamando al [ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) del elemento con IID \_ ITfLangBarItemSink. El elemento usa la **interfaz ITfLangBarItemSink** para notificar a la barra de idioma los cambios, por ejemplo, cuando el elemento está oculto, mostrado, habilitado o deshabilitado.

Se pueden instalar cuatro tipos de elementos de barra de lenguaje y cada una de las interfaces necesarias se crea a partir **de ITfLangBarItem**. Los siguientes son posibles elementos de control **ITfLangBarItem.**



|   Elemento            |    Descripción                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botón        | Un botón de barra de idioma funciona como un botón de comando, un control de alternancia o un menú en la barra de idioma. El objeto debe admitir la interfaz ITfLangBarItemButton.                   |
| Globo       | Un globo de barra de idioma funciona como una notificación emergente en la barra de idioma. El objeto debe admitir la interfaz ITfLangBarItemBalloon.                                       |
| Bitmap        | Un mapa de bits de barra de idioma funciona como un elemento estático en la barra de idioma que muestra un mapa de bits. El objeto debe admitir la interfaz ITfLangBarItemBitmap.                       |
| Botón De mapa de bits | Un botón de mapa de bits de barra de idioma funciona como un elemento de botón en la barra de idioma que muestra texto y un mapa de bits. El objeto debe admitir la interfaz ITfLangBarItemBitmapButton. |



 

## <a name="button-styles"></a>Estilos de botón

Un elemento de botón puede funcionar como cualquiera de las siguientes. La función del elemento de botón viene determinada por las marcas establecidas en el **miembro dwStyle** de la estructura [ \_ LANGBARITEMINFO de TF](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) en el método [ITfLangBarItem::GetInfo.](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo)



|    Elemento           |    Descripción                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Botón        | El botón funciona como un botón de comando estándar. Este estilo de botón se identifica mediante el estilo \_ TF LBI \_ STYLE \_ BTN \_ BUTTON. Se llama a ITfLangBarItemButton::OnClick cuando se hace clic en el elemento. No se usan ITfLangBarItemButton::InitMenu e ITfLangBarItemButton::OnMenuSelect.                                                                                                   |
| Botón de alternancia | El botón funciona como un control de alternancia que puede mantener un estado en el que se ha hecho clic, de forma similar a una casilla. Este estilo de botón se identifica mediante el estilo \_ TF LBI \_ STYLE \_ BTN \_ TOGGLE. Se llama a ITfLangBarItemButton::OnClick cuando se hace clic en el elemento. No se usan ITfLangBarItemButton::InitMenu e ITfLangBarItemButton::OnMenuSelect.                                                  |
| Menú          | El botón funciona como un menú desplegable. Este estilo de botón se identifica mediante el estilo TF \_ LBI \_ STYLE \_ BTN \_ MENU. Cuando se hace clic en el botón, se llama a ITfLangBarItemButton::InitMenu. Cuando el usuario selecciona un elemento en el menú, la barra de idioma llama a ITfLangBarItemButton::OnMenuSelect con el identificador del elemento de menú seleccionado. ITfLangBarItemButton::OnClick no se usa. |



 

## <a name="implementing-a-menu-button"></a>Implementar un botón de menú

Cuando el usuario hace clic en un botón de menú, la barra de idioma llama a [ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu). El elemento agrega elementos al menú mediante la [interfaz ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) pasada a InitMenu.

Para agregar un submenú al menú, llame a [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) con TF \_ LBMENUF \_ SUBMENU. Cuando esto se hace, se devuelve un nuevo **objeto ITfMenu** que representa el submenú en el parámetro *ppMenu* de AddMenuItem. Este nuevo objeto de menú se usa para agregar elementos al submenú.

Cuando el usuario selecciona un elemento en el menú, la barra de idioma llama a [ITfLangBarItemButton::OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) con el identificador del elemento de menú seleccionado.

## <a name="adding-items-to-the-language-bar"></a>Agregar elementos a la barra de idioma

Un servicio de texto debe agregar sus elementos a la barra de lenguaje cuando se llama a su método [ITfTextInputProcessor::Activate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) y quitarlos cuando se llama a [su ITfTextInputProcessor::D eactivate.](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate)

Para agregar un elemento a la barra de lenguaje, el servicio de texto obtiene una interfaz [ITfLangBarItemMgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) mediante una llamada a ITfThreadMgr::QueryInterface con IID \_ ITfLangBarItemMgr. A continuación, el servicio de texto [llama a ITfLangBarItemMgr::AddItem con](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) el puntero al objeto de elemento de la barra de lenguaje.

El servicio de texto debe quitar el elemento cuando esté desactivado. El servicio de texto usa la misma **interfaz ITfLangBarItemMgr** que se usa para agregar los elementos u obtiene otra instancia de la interfaz. A continuación, el servicio de texto llama a [ITfLangBarItemMgr::RemoveItem con](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) el puntero de interfaz del elemento que se va a quitar.

## <a name="extending-system-language-bar-items"></a>Extender elementos de la barra de lenguaje del sistema

TSF proporciona la capacidad de agregar elementos de menú a los menús de la barra de idioma existentes. Esto permite que un servicio de texto agregue elementos al menú de otro servicio de texto sin tener que agregar un botón independiente a la barra de herramientas. Esto también permite que los elementos de menú se organicen en grupos lógicos. Por ejemplo, un servicio de texto que proporciona características adicionales al servicio de texto de voz estándar puede agregar elementos al menú del servicio de texto de voz en lugar de agregar su propio botón de menú de nivel superior.

Un servicio de texto proporciona una extensión de menú de barra de lenguaje mediante la implementación de un objeto que admite la [interfaz ITfSystemLangBarItemSink.](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) Esta interfaz funciona exactamente igual que la [interfaz ITfLangBarItemButton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) para un botón de menú. Cuando se muestra el menú, el servicio de texto extendido llama a [ITfSystemLangBarItemSink::InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu). La extensión agrega elementos al menú mediante la [interfaz ITfMenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) pasada a **InitMenu**. Cuando el usuario selecciona un elemento agregado por la extensión, el servicio de texto extendido llama a [ITfSystemLangBarItemSink::OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) con el identificador del elemento de menú seleccionado.

Para instalar una extensión de menú de barra de idioma, el servicio de texto completa los pasos siguientes.

1.  Obtenga la **interfaz ITfLangBarItem** para que el elemento se extienda mediante una llamada a [ITfLangBarItemMgr::GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) con el **GUID** para el elemento que se va a extender.
2.  Obtenga la **interfaz ITfSource del** elemento que se va a extender llamando a ITfLangBarItem::QueryInterface con IID \_ ITfSource.
3.  Llame [a ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID ITfSystemLangBarItemSink y el puntero al \_ objeto **ITfSystemLangBarItemSink.** Si se produce un error en ITfSource::AdviseSink, el servicio de texto no admite extensiones de menú.

[ITfSource::UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource::AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Compatibilidad con las extensiones de menú de la barra de idioma

Un servicio de texto puede permitir que otros servicios de texto agreguen elementos a los menús de la barra de idioma, como se ha mostrado anteriormente. El servicio de texto que debe publicar su GUID para que el elemento se pueda obtener llamando a [ITfLangBarItemMgr::GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem).

Para admitir extensiones de menú, el servicio de texto debe admitir la [interfaz ITfSource.](/windows/desktop/api/msctf/nn-msctf-itfsource) Los pasos siguientes habilitan la compatibilidad con una o varias extensiones de menú.

1.  Cuando se llama a [ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) con IID ITfSystemLangBarItemSink, el servicio de texto debe almacenar la interfaz \_ **ITfSystemLangBarItemSink** y devolver un valor de cookie que identifique la extensión.
2.  Cuando se llama a [ITfLangBarItemButton::InitMenu,](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) el servicio de texto llama al método [ITfSystemLangBarItemSink::InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) de la extensión. El servicio de texto debe implementar una manera de identificar los elementos de menú agregados por la extensión en lugar de los elementos agregados por el propio servicio de texto.
3.  Cuando se llama a [ITfLangBarItemButton::OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) con un identificador de elemento de menú que pertenece a una extensión, el servicio de texto llama al método **ITfSystemLangBarItemSink::OnMenuSelect** de las extensiones.
4.  Cuando [se llama a ITfSource::UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) con la cookie adecuada, el servicio de texto quita la extensión de menú.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Text Services Framework](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de lenguaje (aplicaciones)](language-bar-app.md)
</dt> </dl>

 

 
