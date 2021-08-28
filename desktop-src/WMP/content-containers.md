---
title: Contenedores de contenido
description: Contenedores de contenido
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Reproductor de Windows Media en línea, contenedores de contenido
- tiendas en línea, contenedores de contenido
- tiendas en línea de tipo 1, contenedores de contenido
- Reproductor de Windows Media tiendas en línea, interfaz IWMPContentContainer
- online stores,IWMPContentContainer (interfaz)
- tipo 1 online stores,IWMPContentContainer (interfaz)
- Reproductor de Windows Media,contenedores de contenido
- Reproductor de Windows Media interfaz IWMPContentContainer
- contenedores de contenido
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c582a04bd37e54a40f952402343c09fb7243fc07377ef7f507cc76f11390357c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123685"
---
# <a name="content-containers"></a>Contenedores de contenido

Reproductor de Windows Media contenedores de contenido para representar el contenido multimedia digital en una transacción de descarga o compra de suscripción. Un contenedor de contenido se representa mediante la **interfaz IWMPContentContainer.** Un contenedor de contenido puede contener una lista de contenido relacionado, como un álbum o un conjunto de elementos de contenido no relacionados, o *pistas*. Puede usar la **interfaz IWMPContentContainer** para enumerar las pistas del contenedor de contenido y recuperar el precio de cada pista. También puede recuperar información sobre el propio contenedor de contenido, como el identificador del contenedor, el tipo de contenido del contenedor y el precio total de las pistas del contenedor (que puede diferir de la suma de los precios de las pistas individuales, como en el caso de una compra de álbum).

Para proporcionar un mecanismo para empaquetar varios contenedores de contenido en un único objeto, Reproductor de Windows Media admite la **interfaz IWMPContentContainerList.** **IWMPContentContainerList proporciona** métodos para enumerar y recuperar los contenedores de contenido de la lista. Para detectar si la lista de contenedores de contenido representa una compra o una descarga de suscripción, llame a [IWMPContentContainerList::GetTransactionType para](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) recuperar un [valor WMPTransactionType.](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentContainer (interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**IWMPContentContainerList (Interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




