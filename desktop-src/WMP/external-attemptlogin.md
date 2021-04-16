---
title: External. attemptLogin (método)
description: El método attemptLogin muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- método attemptLogin de Windows Media Player
- método attemptLogin de Windows Media Player, clase externa
- Clase externa Windows Media Player, método attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699729"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="e935c-106">External. attemptLogin (método)</span><span class="sxs-lookup"><span data-stu-id="e935c-106">External.attemptLogin method</span></span>

<span data-ttu-id="e935c-107">El método **attemptLogin** muestra un cuadro de diálogo para que el usuario pueda intentar iniciar sesión en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e935c-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="e935c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e935c-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="e935c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e935c-109">Parameters</span></span>

<span data-ttu-id="e935c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e935c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e935c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e935c-111">Return value</span></span>

<span data-ttu-id="e935c-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e935c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e935c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e935c-113">Remarks</span></span>

<span data-ttu-id="e935c-114">Si el intento de inicio de sesión produce un cambio en el estado de inicio de sesión, Windows Media Player genera el evento [OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="e935c-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e935c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e935c-115">Requirements</span></span>



| <span data-ttu-id="e935c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e935c-116">Requirement</span></span> | <span data-ttu-id="e935c-117">Value</span><span class="sxs-lookup"><span data-stu-id="e935c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e935c-118">Versión</span><span class="sxs-lookup"><span data-stu-id="e935c-118">Version</span></span><br/> | <span data-ttu-id="e935c-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e935c-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e935c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e935c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e935c-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e935c-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e935c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e935c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e935c-123">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e935c-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e935c-124">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="e935c-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="e935c-125">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="e935c-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="e935c-126">**IWMPContentPartner:: login**</span><span class="sxs-lookup"><span data-stu-id="e935c-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="e935c-127">**Administrar inicio de sesión**</span><span class="sxs-lookup"><span data-stu-id="e935c-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





