---
title: External. Authenticate (método)
description: El método Authenticate inicia un intento de autenticación del usuario.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- autenticación de Windows de método Media Player
- método de autenticación de Windows Media Player, clase externa
- Clase externa Windows Media Player, método Authenticate
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699728"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="a867d-106">External. Authenticate (método)</span><span class="sxs-lookup"><span data-stu-id="a867d-106">External.authenticate method</span></span>

<span data-ttu-id="a867d-107">El método **Authenticate** inicia un intento de autenticación del usuario.</span><span class="sxs-lookup"><span data-stu-id="a867d-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a867d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a867d-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="a867d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a867d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a867d-110">*AuthenticationIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a867d-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a867d-111">**Número** (**largo**) que especifica el índice de una página web de autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="a867d-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a867d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a867d-112">Return value</span></span>

<span data-ttu-id="a867d-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a867d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a867d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a867d-114">Remarks</span></span>

<span data-ttu-id="a867d-115">Algunos vínculos de una página de detección tienen destinos que deben mostrarse solo después de que el usuario se haya autenticado.</span><span class="sxs-lookup"><span data-stu-id="a867d-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="a867d-116">En la página detección, en Windows Media Player y en el complemento de la tienda en línea, siga los pasos que se indican a continuación para autenticar al usuario y mostrar la Página Web de destino:</span><span class="sxs-lookup"><span data-stu-id="a867d-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="a867d-117">El script de una página de detección llama a la *externa*. método de **autenticación** .</span><span class="sxs-lookup"><span data-stu-id="a867d-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="a867d-118">Windows Media Player muestra un cuadro de diálogo para obtener un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="a867d-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="a867d-119">Windows Media Player llama a [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), que inicia el intento de autenticación y vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a867d-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="a867d-120">Cuando se completa el intento de autenticación, el complemento de la tienda en línea llama a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnAuthResult y un valor booleano que indica si el intento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a867d-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="a867d-121">Si el intento de autenticación se realizó correctamente, Windows Media Player llama a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), pasando g \_ szItemInfo \_ AuthenticationSuccessURL, para obtener la dirección URL de una página web de autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="a867d-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="a867d-122">En esta llamada, Windows Media Player pasa el mismo índice que la página de detección pasada a la *externa*. método de **autenticación** .</span><span class="sxs-lookup"><span data-stu-id="a867d-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="a867d-123">Windows Media Player muestra la Página Web de autenticación correcta.</span><span class="sxs-lookup"><span data-stu-id="a867d-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="a867d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a867d-124">Requirements</span></span>



| <span data-ttu-id="a867d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a867d-125">Requirement</span></span> | <span data-ttu-id="a867d-126">Value</span><span class="sxs-lookup"><span data-stu-id="a867d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a867d-127">Versión</span><span class="sxs-lookup"><span data-stu-id="a867d-127">Version</span></span><br/> | <span data-ttu-id="a867d-128">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="a867d-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="a867d-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a867d-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="a867d-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a867d-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a867d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a867d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a867d-132">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a867d-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a867d-133">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="a867d-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="a867d-134">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="a867d-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





