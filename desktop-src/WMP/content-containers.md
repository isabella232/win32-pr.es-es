---
title: Contenedores de contenido
description: Contenedores de contenido
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Reproductor de Windows Media en línea, contenedores de contenido
- tiendas en línea, contenedores de contenido
- tiendas en línea de tipo 1, contenedores de contenido
- Reproductor de Windows Media en línea, interfaz IWMPContentContainer
- online stores,IWMPContentContainer (interfaz)
- tipo 1 online stores,IWMPContentContainer (interfaz)
- Reproductor de Windows Media,contenedores de contenido
- Reproductor de Windows Media interfaz IWMPContentContainer
- contenedores de contenido
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967736"
---
# <a name="content-containers"></a>Contenedores de contenido

Reproductor de Windows Media contenedores de contenido para representar el contenido multimedia digital en una transacción de descarga o compra de suscripción. Un contenedor de contenido se representa mediante la **interfaz IWMPContentContainer.** Un contenedor de contenido puede contener una lista de contenido relacionado, como un álbum o un conjunto de elementos de contenido no relacionados, o *pistas*. Puede usar la **interfaz IWMPContentContainer** para enumerar las pistas del contenedor de contenido y recuperar el precio de cada pista. También puede recuperar información sobre el propio contenedor de contenido, como el identificador del contenedor, el tipo de contenido del contenedor y el precio total de las pistas del contenedor (que pueden diferir de la suma de los precios de las pistas individuales, como en el caso de una compra de álbum).

Para proporcionar un mecanismo para empaquetar varios contenedores de contenido en un único objeto, Reproductor de Windows Media admite la **interfaz IWMPContentContainerList.** **IWMPContentContainerList proporciona** métodos para enumerar y recuperar los contenedores de contenido de la lista. Para detectar si la lista de contenedores de contenido representa una compra o una descarga de suscripción, llame a [IWMPContentContainerList::GetTransactionType para](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) recuperar un [valor WMPTransactionType.](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentContainer (interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**IWMPContentContainerList (Interfaz)**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




