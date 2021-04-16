---
title: External. showPopup (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. showPopup (método)
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup (método) de Windows Media Player
- showPopup (método) Windows Media Player, clase externa
- Clase externa Windows Media Player, método showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699414"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="6e899-107">External. showPopup (método)</span><span class="sxs-lookup"><span data-stu-id="6e899-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="6e899-108">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="6e899-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6e899-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6e899-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6e899-110">El método **ShowPopup** indica a Windows Media Player que muestre una página web emergente; es decir, una página web que aparece en una ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="6e899-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e899-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e899-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="6e899-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e899-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e899-113">*PopupIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e899-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e899-114">**Número** (**Long**) que especifica el índice de la página web emergente.</span><span class="sxs-lookup"><span data-stu-id="6e899-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="6e899-115">*Parámetros* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6e899-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e899-116">**Cadena** que Windows Media Player anexa a la dirección URL de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="6e899-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e899-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e899-117">Return value</span></span>

<span data-ttu-id="6e899-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e899-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e899-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e899-119">Remarks</span></span>

<span data-ttu-id="6e899-120">Windows Media Player no interpreta el índice emergente.</span><span class="sxs-lookup"><span data-stu-id="6e899-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="6e899-121">Los índices que identifican las páginas web emergentes se crean en la tienda en línea y solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="6e899-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="6e899-122">En los pasos siguientes se muestra cómo Windows Media Player utiliza los parámetros del método **ShowPopup** para crear una dirección URL para la ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="6e899-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="6e899-123">El script de una página de detección llama a **ShowPopup**, pasando un entero en *PopupIndex* y una cadena en *parámetros*.</span><span class="sxs-lookup"><span data-stu-id="6e899-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="6e899-124">Windows Media Player pasa el índice a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para recuperar la dirección URL de la página web que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="6e899-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="6e899-125">Windows Media Player anexa *parámetros* a la dirección URL como una cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="6e899-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="6e899-126">Por ejemplo, si **GetItemInfo** devuelve " https://www.Proseware.com/Pages/Popup1.htm " y *los parámetros* son iguales a "DlgX = 800&DlgY = 400&Greeting = HI", Windows Media Player crea la siguiente dirección URL:</span><span class="sxs-lookup"><span data-stu-id="6e899-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="6e899-127">Puede usar *parámetros* para especificar el tamaño de la ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="6e899-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="6e899-128">Por ejemplo, si establece *los parámetros* en "DlgX = 800&DlgY = 400", la ventana emergente tendrá un tamaño de 800 píxeles por 400 píxeles.</span><span class="sxs-lookup"><span data-stu-id="6e899-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e899-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e899-129">Requirements</span></span>



| <span data-ttu-id="6e899-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e899-130">Requirement</span></span> | <span data-ttu-id="6e899-131">Value</span><span class="sxs-lookup"><span data-stu-id="6e899-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e899-132">Versión</span><span class="sxs-lookup"><span data-stu-id="6e899-132">Version</span></span><br/> | <span data-ttu-id="6e899-133">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="6e899-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="6e899-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e899-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="6e899-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e899-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e899-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e899-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e899-137">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6e899-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





