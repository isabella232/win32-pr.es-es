---
title: External. accountType
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad accountType recupera el tipo de cuenta del usuario actual.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Media Player de Windows externa. accountType
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699874"
---
# <a name="externalaccounttype"></a><span data-ttu-id="8f6ea-106">External. accountType</span><span class="sxs-lookup"><span data-stu-id="8f6ea-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="8f6ea-107">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="8f6ea-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="8f6ea-109">La propiedad **accountType** recupera el tipo de cuenta del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="8f6ea-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8f6ea-110">Possible Values</span></span>

<span data-ttu-id="8f6ea-111">Esta propiedad es una **cadena** de solo lectura que representa el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="8f6ea-112">Las cadenas que representan varios tipos de cuenta se definen en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f6ea-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f6ea-113">Remarks</span></span>

<span data-ttu-id="8f6ea-114">Esta propiedad recupera el tipo de cuenta llamando al método [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , que se implementa mediante el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="8f6ea-115">Si el usuario actual ha iniciado sesión en la tienda en línea o el complemento ha almacenado en caché las credenciales del usuario, el método **getContentPartnerInfo** puede determinar el tipo de cuenta del usuario y devolverlo a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="8f6ea-116">El tipo de cuenta es una cadena que Windows Media Player no interpreta.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="8f6ea-117">En su lugar, Windows Media Player pasa la cadena del complemento de la tienda en línea al script en la página de detección de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="8f6ea-118">Si el usuario actual no ha iniciado sesión en la tienda en línea y el complemento de la tienda en línea no tiene credenciales almacenadas en caché para el usuario, esta propiedad recupera cualquier cadena que devuelva el método **getContentPartnerInfo** en esa situación.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6ea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f6ea-119">Requirements</span></span>



| <span data-ttu-id="8f6ea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f6ea-120">Requirement</span></span> | <span data-ttu-id="8f6ea-121">Value</span><span class="sxs-lookup"><span data-stu-id="8f6ea-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6ea-122">Versión</span><span class="sxs-lookup"><span data-stu-id="8f6ea-122">Version</span></span><br/> | <span data-ttu-id="8f6ea-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="8f6ea-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="8f6ea-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f6ea-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f6ea-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f6ea-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6ea-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f6ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6ea-127">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="8f6ea-128">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="8f6ea-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





