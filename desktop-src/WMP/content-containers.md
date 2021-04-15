---
title: Contenedores de contenido
description: Contenedores de contenido
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player tiendas en línea, contenedores de contenido
- tiendas en línea, contenedores de contenido
- tipo 1 almacenes en línea, contenedores de contenido
- Windows Media Player tiendas en línea, interfaz IWMPContentContainer
- tiendas en línea, interfaz IWMPContentContainer
- tipo 1 tiendas en línea, interfaz IWMPContentContainer
- Windows Media Player, contenedores de contenido
- Windows Media Player, interfaz IWMPContentContainer
- contenedores de contenido
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "105695570"
---
# <a name="content-containers"></a>Contenedores de contenido

Windows Media Player utiliza contenedores de contenido para representar el contenido multimedia digital en una transacción de descarga o compra de suscripción. Un contenedor de contenido se representa mediante la interfaz **IWMPContentContainer** . Un contenedor de contenido podría contener una lista de contenido relacionado, como un álbum, o un conjunto de elementos de contenido no relacionados o *pistas*. Puede usar la interfaz **IWMPContentContainer** para enumerar las pistas del contenedor de contenido y recuperar el precio de cada pista. También puede recuperar información sobre el propio contenedor de contenido, como el identificador del contenedor, el tipo de contenido del contenedor y el precio total de las pistas del contenedor (que podrían diferir de la suma de los precios de las pistas individuales, como en el caso de una compra de álbum).

Para proporcionar un mecanismo para empaquetar varios contenedores de contenido en un único objeto, Windows Media Player admite la interfaz **IWMPContentContainerList** . **IWMPContentContainerList** proporciona métodos para enumerar y recuperar los contenedores de contenido de la lista. Para detectar si la lista de contenedores de contenido representa una descarga de compra o de suscripción, llame a [IWMPContentContainerList:: GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) para recuperar un valor de [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interfaz IWMPContentContainer**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[**Interfaz IWMPContentContainerList**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




