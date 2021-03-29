---
title: Mostrar cuadros de diálogo
description: Mostrar cuadros de diálogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player tiendas en línea, Mostrar cuadros de diálogo
- tiendas en línea, Mostrar cuadros de diálogo
- tipo 1 tiendas en línea, Mostrar cuadros de diálogo
- Windows Media Player tiendas en línea, cuadros de diálogo
- tiendas en línea, cuadros de diálogo
- tipo 1 tiendas en línea, cuadros de diálogo
- Mostrar cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788775"
---
# <a name="displaying-dialog-boxes"></a>Mostrar cuadros de diálogo

La tienda en línea puede invocar cuadros de diálogo a través de Windows Media Player. Para ello, llame a [external. ShowPopup](external-showpopup.md) desde el código de script de la página de detección y proporcione un valor de índice personalizado que represente el cuadro de diálogo que se va a mostrar. Este valor de índice solo tiene significado para el código de la tienda en línea; Windows Media Player no interpreta este valor. Windows Media Player llama entonces a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g \_ szItemInfo \_ PopupURL para el parámetro *bstrInfoName* y el número de índice del parámetro *pContext* . A continuación, el complemento devuelve un **BSTR** que contiene la dirección URL de la página web que se va a mostrar en el cuadro de diálogo y el reproductor muestra el cuadro de diálogo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




