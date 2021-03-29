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
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="c5fee-110">Mostrar cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="c5fee-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="c5fee-111">La tienda en línea puede invocar cuadros de diálogo a través de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c5fee-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="c5fee-112">Para ello, llame a [external. ShowPopup](external-showpopup.md) desde el código de script de la página de detección y proporcione un valor de índice personalizado que represente el cuadro de diálogo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c5fee-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="c5fee-113">Este valor de índice solo tiene significado para el código de la tienda en línea; Windows Media Player no interpreta este valor.</span><span class="sxs-lookup"><span data-stu-id="c5fee-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="c5fee-114">Windows Media Player llama entonces a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g \_ szItemInfo \_ PopupURL para el parámetro *bstrInfoName* y el número de índice del parámetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="c5fee-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="c5fee-115">A continuación, el complemento devuelve un **BSTR** que contiene la dirección URL de la página web que se va a mostrar en el cuadro de diálogo y el reproductor muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c5fee-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5fee-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5fee-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5fee-117">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="c5fee-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




