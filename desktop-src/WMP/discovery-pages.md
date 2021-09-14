---
title: Páginas de detección
description: Páginas de detección
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Reproductor de Windows Media en línea,páginas de detección
- tiendas en línea, páginas de detección
- tiendas en línea de tipo 1, páginas de detección
- Reproductor de Windows Media biblioteca, páginas de detección
- biblioteca, páginas de detección
- páginas de detección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068458"
---
# <a name="discovery-pages"></a>Páginas de detección

Si la tienda en línea activa es de tipo 1, Reproductor de Windows Media muestra el contenido de la tienda en su interfaz de usuario. El control de vista de árbol de biblioteca tiene un nodo para el almacén en línea. Cuando el usuario hace clic en ese nodo o en cualquiera de sus subnodos, Reproductor de Windows Media muestra el contenido de la tienda en línea en el panel de detalles.

A medida que el usuario interactúa con el contenido de la tienda en línea en el control de vista de árbol o en el panel de detalles, Reproductor de Windows Media muestra páginas web, denominadas páginas de detección, proporcionadas por la tienda en línea. Las páginas de detección proporcionan información adicional sobre la música a medida que el usuario examina el catálogo de la tienda en línea. Las páginas de detección Reproductor de Windows Media a través de las propiedades, métodos y eventos del [objeto externo](external-object-for-type-1-online-stores.md).

Cada Reproductor de Windows Media cambia su vista del contenido de la tienda en línea, llama a [IWMPContentPartner::GetTemplate,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)implementado por el complemento de la tienda en línea, para obtener la dirección URL de la página de detección que se mostrará con la nueva vista.

La vista del contenido de la tienda en línea de Reproductor de Windows Media se caracteriza por cinco elementos de información: tarea, tipo de ubicación, identificador de ubicación, tipo de elemento seleccionado e identificador de elemento seleccionado. Reproductor de Windows Media proporciona esos cinco elementos al método **GetTemplate** en los parámetros de tarea *,* *location*, *pContext,* *clickLocation* y *pClickContext.* Reproductor de Windows Media pone esos cinco elementos a disposición de las páginas de detección de la tarea *,* *libraryLocationType*, *libraryLocationID,* *selectedItemType y* las propiedades *selectedItemID* del **objeto External.** Para obtener más información sobre cómo Reproductor de Windows Media especifica su vista del contenido de la tienda en línea, vea [Ubicación y elemento seleccionado.](location-and-selected-item.md)

Además de permitir que una página de detección  se comunique con Reproductor de Windows Media, el objeto External permite que una página de detección se comunique con el complemento del almacén en línea. Cuando esto sucede, Reproductor de Windows Media actúa como un puente entre la página de detección y el complemento. Por ejemplo, la página de detección puede llamar a [External.sendMessage](external-sendmessage.md) para enviar un mensaje personalizado al complemento. Reproductor de Windows Media esta llamada al método y, a su vez, llama a [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) para pasar el mensaje al complemento. Cuando el complemento haya terminado de procesar el mensaje, llama a [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete). Reproductor de Windows Media a la página de detección generando el [evento External.OnSendMessageComplete.](external-onsendmessagecomplete-event.md)

El **objeto External** también proporciona una manera de que una página de detección se comunique con otra página de detección. Cuando el script de una página de detección llama a [External.changeView,](external-changeview.md)el script puede proporcionar una cadena en el *parámetro ViewParams.* Reproductor de Windows Media no interpreta la cadena *ViewParams,* pero hace que la cadena esté disponible para la siguiente página de detección en la [propiedad External.viewParameters.](external-viewparameters.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Ubicación y elemento seleccionado**](location-and-selected-item.md)
</dt> </dl>

 

 




