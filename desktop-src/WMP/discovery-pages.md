---
title: Páginas de detección
description: Páginas de detección
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player tiendas en línea, páginas de detección
- tiendas en línea, páginas de detección
- tipo 1 tiendas en línea, páginas de detección
- Biblioteca de Media Player de Windows, páginas de detección
- Biblioteca, páginas de detección
- páginas de detección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788776"
---
# <a name="discovery-pages"></a>Páginas de detección

Si la tienda en línea activa es un almacén de tipo 1, Windows Media Player muestra el contenido del almacén en su interfaz de usuario. El control de vista de árbol de la biblioteca tiene un nodo para la tienda en línea. Cuando el usuario hace clic en ese nodo o en cualquiera de sus subnodos, Windows Media Player muestra el contenido de la tienda en línea en el panel de detalles.

A medida que el usuario interactúa con el contenido de la tienda en línea en el control de vista de árbol o en el panel de detalles, Windows Media Player muestra las páginas web, denominadas *páginas de detección*, que proporciona la tienda en línea. Las páginas de detección proporcionan información adicional sobre la música a medida que el usuario examina el catálogo de la tienda en línea. Las páginas de detección se comunican con Windows Media Player a través de las propiedades, métodos y eventos del [objeto externo](external-object-for-type-1-online-stores.md).

Cada vez que Windows Media Player cambia su vista del contenido de la tienda en línea, llama a [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate), implementada por el complemento de la tienda en línea, para obtener la dirección URL de la página de detección que se va a mostrar con la nueva vista.

La vista del contenido de la tienda en línea en Windows Media Player se caracteriza por cinco fragmentos de información: tarea, tipo de ubicación, ID. de ubicación, tipo de elemento seleccionado y identificador de elemento seleccionado. Windows Media Player proporciona esos cinco elementos al método **GetTemplate** en los parámetros *Task*, *Location*, *pContext*, *clickLocation* y *pClickContext* . Windows Media Player hace que esos cinco elementos estén disponibles para las páginas de detección en las propiedades *Task*, *libraryLocationType*, *libraryLocationID*, *selectedItemType* y *selectedItemID* del objeto **externo** . Para obtener más información acerca de cómo Windows Media Player especifica su vista del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).

Además de permitir que una página de detección se comunique con Windows Media Player, el objeto **externo** permite que una página de detección se comunique con el complemento de la tienda en línea. Cuando esto sucede, Windows Media Player actúa como un puente entre la página de detección y el complemento. Por ejemplo, la página de detección puede llamar a [external. SendMessage](external-sendmessage.md) para enviar un mensaje personalizado al complemento. Windows Media Player recibe esta llamada al método y, a su vez, llama a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) para pasar el mensaje al complemento. Cuando el complemento ha terminado de procesar el mensaje, llama a [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete). Windows Media Player notifica entonces a la página de detección generando el evento [external. OnSendMessageComplete](external-onsendmessagecomplete-event.md) .

El objeto **externo** también proporciona una manera de que una página de detección se comunique con otra página de detección. Cuando el script de una página de detección llama a [external. changeView](external-changeview.md), el script puede proporcionar una cadena en el parámetro *ViewParams* . Windows Media Player no interpreta la cadena *ViewParams* , pero hace que la cadena esté disponible para la siguiente página de detección en la propiedad [external. viewParameters](external-viewparameters.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 




