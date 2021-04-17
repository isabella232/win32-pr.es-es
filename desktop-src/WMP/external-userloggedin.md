---
title: External. userLoggedIn
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. userLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- Media Player de Windows externa. userLoggedIn
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699722"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="1d8aa-105">External. userLoggedIn</span><span class="sxs-lookup"><span data-stu-id="1d8aa-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="1d8aa-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1d8aa-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1d8aa-108">La propiedad **userLoggedIn** recupera un valor que indica si el usuario ha iniciado sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8aa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d8aa-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="1d8aa-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1d8aa-110">Possible Values</span></span>

<span data-ttu-id="1d8aa-111">Esta propiedad es un **valor booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="1d8aa-112">**True** indica que el usuario ha iniciado sesión y **false** indica que el usuario ha cerrado la sesión.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8aa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d8aa-113">Requirements</span></span>



| <span data-ttu-id="1d8aa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8aa-114">Requirement</span></span> | <span data-ttu-id="1d8aa-115">Value</span><span class="sxs-lookup"><span data-stu-id="1d8aa-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8aa-116">Versión</span><span class="sxs-lookup"><span data-stu-id="1d8aa-116">Version</span></span><br/> | <span data-ttu-id="1d8aa-117">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1d8aa-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="1d8aa-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d8aa-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d8aa-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d8aa-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8aa-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d8aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8aa-121">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="1d8aa-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="1d8aa-122">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="1d8aa-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="1d8aa-123">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="1d8aa-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





