---
title: Compra de contenido multimedia
description: Compra de contenido multimedia
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player tiendas en línea, contenido multimedia de compra
- tiendas en línea, contenido multimedia de compra
- tipo 1 tiendas en línea, contenido multimedia de compra
- Windows Media Player tiendas en línea, compras de contenido multimedia
- tiendas en línea, compras de contenido multimedia
- tipo 1 tiendas en línea, compras de contenido multimedia
- contenido multimedia, compras
- compra de contenido multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994929"
---
# <a name="purchasing-media-content"></a>Compra de contenido multimedia

Cuando Windows Media Player muestra el contenido de la música en la vista de árbol de la biblioteca, la interfaz de usuario incluye los elementos en los que el usuario puede hacer clic para comprar el contenido. Por ejemplo, el usuario puede hacer clic en un botón para comprar una canción individual o comprar un álbum completo.

Si la tienda en línea activa es un almacén de tipo 1, Windows Media Player tiene acceso a los precios de seguimiento, álbum y lista en el catálogo de la tienda en línea. Los precios del catálogo son cadenas con un formato que solo entiende la tienda en línea. Windows Media Player no interpreta las cadenas de precio; simplemente se muestran en elementos de la interfaz de usuario como botones de compra.

Cuando Windows Media Player configura una compra para un conjunto de elementos multimedia, pasa los identificadores y los precios de los elementos multimedia al complemento de asociado de contenido mediante una llamada a [IWMPContentPartner:: CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent). En ese momento, el complemento puede inspeccionar los precios proporcionados por el reproductor. Estos son los precios que el usuario espera pagar; es decir, los precios que el reproductor muestra al usuario. En función de los identificadores de medios y los precios proporcionados por el reproductor, el complemento calcula un precio total, que devuelve al reproductor en el parámetro *bstrTotalPrice* . Los precios que el jugador pasa a **CanBuySilent** proporcionan información sobre el complemento, pero no obligan a que el complemento devuelva un precio total determinado. El complemento puede calcular el precio total según sea posible.

Además de calcular el precio total de una compra, **CanBuySilent** determina si el purchace puede continuar de forma silenciosa. es decir, sin mostrar un cuadro de diálogo. Si **CanBuySilent** devuelve **True**, Windows Media Player simplemente cambia el texto del botón comprar para solicitar al usuario que confirme la compra. Si **CanBuySilent** devuelve **False**, Windows Media Player muestra un cuadro de diálogo que pide al usuario que confirme la compra. El cuadro de diálogo proporciona al usuario información que resume la compra como el número de álbumes, el número de pistas individuales y el precio total (devuelto por el complemento).

Una vez que el usuario confirma la compra, el reproductor llama a [IWMPContentPartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy). Esta llamada al método proporciona el complemento con la misma lista de contenedores de contenido que **CanBuySilent**. Al llamar a **Buy**, Windows Media Player proporciona también una cookie (simplemente un valor **DWORD** , único para la sesión) que el complemento puede utilizar para identificar la transacción. Cuando se completa la transacción, el complemento debe llamar a [IWMPContentPartnerCallback:: BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete), pasando el valor de cookie original para el parámetro *dwBuyCookie* , para notificar al reproductor que la transacción ha finalizado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




