---
title: Mostrar cuadros de diálogo
description: Mostrar cuadros de diálogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Reproductor de Windows Media en línea, mostrar cuadros de diálogo
- tiendas en línea, mostrar cuadros de diálogo
- tiendas en línea de tipo 1, mostrar cuadros de diálogo
- Reproductor de Windows Media en línea, cuadros de diálogo
- tiendas en línea, cuadros de diálogo
- tiendas en línea de tipo 1, cuadros de diálogo
- mostrar cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997275"
---
# <a name="displaying-dialog-boxes"></a>Mostrar cuadros de diálogo

El almacén en línea puede invocar cuadros de diálogo a través Reproductor de Windows Media. Para ello, llame a [External.showPopup](external-showpopup.md) desde el código de script de la página de detección, proporcionando un valor de índice personalizado que representa el cuadro de diálogo que se va a mostrar. Este valor de índice solo tiene significado para el código de la tienda en línea; Reproductor de Windows Media no interpreta este valor. Reproductor de Windows Media llama a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g szItemInfo PopupURL para el \_ \_ parámetro *bstrInfoName* y el número de índice para el *parámetro pContext.* A continuación, el complemento devuelve un **BSTR** que contiene la dirección URL de la página web que se va a mostrar en el cuadro de diálogo y el reproductor muestra el cuadro de diálogo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




