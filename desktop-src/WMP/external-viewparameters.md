---
title: External. viewParameters
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Media Player de Windows externa. viewParameters
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699718"
---
# <a name="externalviewparameters"></a><span data-ttu-id="f1c13-105">External. viewParameters</span><span class="sxs-lookup"><span data-stu-id="f1c13-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="f1c13-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="f1c13-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f1c13-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f1c13-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f1c13-108">La propiedad **viewParameters** recupera los parámetros asociados a la vista actual en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f1c13-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c13-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1c13-109">Syntax</span></span>

<span data-ttu-id="f1c13-110">**Window. external. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="f1c13-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f1c13-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f1c13-111">Possible Values</span></span>

<span data-ttu-id="f1c13-112">Esta propiedad devuelve una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1c13-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1c13-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1c13-113">Remarks</span></span>

<span data-ttu-id="f1c13-114">Esta propiedad recupera los parámetros que se establecieron previamente en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f1c13-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="f1c13-115">Por ejemplo, la tienda en línea puede especificar parámetros de vista en el parámetro *ViewParams* del método [changeView](external-changeview.md) o el parámetro *params* del método [changeViewOnlineList](external-changeviewonlinelist.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c13-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="f1c13-116">Los parámetros de vista no se interpretan en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f1c13-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="f1c13-117">Los crea la tienda en línea y solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f1c13-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c13-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c13-118">Requirements</span></span>



| <span data-ttu-id="f1c13-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c13-119">Requirement</span></span> | <span data-ttu-id="f1c13-120">Value</span><span class="sxs-lookup"><span data-stu-id="f1c13-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c13-121">Versión</span><span class="sxs-lookup"><span data-stu-id="f1c13-121">Version</span></span><br/> | <span data-ttu-id="f1c13-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f1c13-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f1c13-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1c13-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1c13-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1c13-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c13-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1c13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c13-126">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f1c13-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





