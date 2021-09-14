---
title: Compra de contenido multimedia
description: Compra de contenido multimedia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Reproductor de Windows Media en línea, comprar contenido multimedia
- tiendas en línea, comprar contenido multimedia
- tiendas en línea de tipo 1, comprar contenido multimedia
- Reproductor de Windows Media en línea, compras de contenido multimedia
- tiendas en línea, compras de contenido multimedia
- tiendas en línea de tipo 1, compras de contenido multimedia
- contenido multimedia, compra
- comprar contenido multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073233"
---
# <a name="purchasing-media-content"></a>Compra de contenido multimedia

Cuando Reproductor de Windows Media contenido de música en la vista de árbol de biblioteca, la interfaz de usuario incluye elementos en los que el usuario puede hacer clic para comprar el contenido. Por ejemplo, el usuario podría hacer clic en un botón para comprar una canción individual o para comprar un álbum completo.

Si la tienda en línea activa es de tipo 1, Reproductor de Windows Media tiene acceso a los precios de seguimiento, álbum y lista en el catálogo de la tienda en línea. Esos precios del catálogo son cadenas que tienen un formato que solo entiende la tienda en línea. Reproductor de Windows Media no interpreta las cadenas de precio; simplemente los muestra en elementos de la interfaz de usuario, como los botones Comprar.

Cuando Reproductor de Windows Media una compra para un conjunto de elementos multimedia, pasa los ID y los precios de los elementos multimedia al complemento del asociado de contenido mediante una llamada a [IWMPContentPartner::CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). En ese momento, el complemento puede inspeccionar los precios proporcionados por el reproductor. Estos son los precios que el usuario espera pagar; es decir, los precios que el reproductor muestra al usuario. En función de los id. de medios y los precios proporcionados por el reproductor, el complemento calcula un precio total, que devuelve al reproductor en el *parámetro bstrTotalPrice.* Los precios que el jugador pasa a **CanBuySilent** proporcionan información al complemento, pero no obligan al complemento a devolver un precio total determinado. El complemento puede calcular el precio total según le conste.

Además de calcular el precio total de una compra, **CanBuySilent** determina si la purga puede continuar en modo silencioso. es decir, sin mostrar un cuadro de diálogo. Si **CanBuySilent** devuelve **True,** Reproductor de Windows Media simplemente cambia el texto del botón Comprar para pedir al usuario que confirme la compra. Si **CanBuySilent** devuelve **False,** Reproductor de Windows Media un cuadro de diálogo que solicita al usuario que confirme la compra. El cuadro de diálogo proporciona al usuario información que resume la compra, como el número de álbumes, el número de pistas individuales y el precio total (tal como lo devuelve el complemento).

Una vez que el usuario confirma la compra, el reproductor llama a [IWMPContentPartner::Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy). Esta llamada al método proporciona al complemento la misma lista de contenedores de contenido que **CanBuySilent.** Al llamar **a Comprar**, Reproductor de Windows Media también proporciona una cookie (simplemente un valor **DWORD,** único para la sesión) que el complemento puede usar para identificar la transacción. Cuando se completa la transacción, el complemento debe llamar a [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), pasando el valor de cookie original para el parámetro *dwBuyCookie,* para notificar al reproductor que la transacción ha finalizado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




