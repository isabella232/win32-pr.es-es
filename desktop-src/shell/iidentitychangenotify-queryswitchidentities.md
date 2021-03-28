---
description: Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify:: QuerySwitchIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909518"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a><span data-ttu-id="0db5b-103">IIdentityChangeNotify:: QuerySwitchIdentities (método)</span><span class="sxs-lookup"><span data-stu-id="0db5b-103">IIdentityChangeNotify::QuerySwitchIdentities method</span></span>

<span data-ttu-id="0db5b-104">\[**QuerySwitchIdentities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0db5b-104">\[**QuerySwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0db5b-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="0db5b-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="0db5b-106">Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.</span><span class="sxs-lookup"><span data-stu-id="0db5b-106">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db5b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0db5b-107">Syntax</span></span>


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="0db5b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0db5b-108">Parameters</span></span>

<span data-ttu-id="0db5b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0db5b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0db5b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0db5b-110">Return value</span></span>

<span data-ttu-id="0db5b-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0db5b-111">Type: **HRESULT**</span></span>

<span data-ttu-id="0db5b-112">Resultado de la consulta switch.</span><span class="sxs-lookup"><span data-stu-id="0db5b-112">Result of the switch query.</span></span> <span data-ttu-id="0db5b-113">Si el conmutador debe continuar, vuelva a ser \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0db5b-113">If the switch should proceed, return S\_OK.</span></span> <span data-ttu-id="0db5b-114">De lo contrario, devuelva \_ \_ el modificador de proceso cancelado \_ para indicar que se debe anular el cambio de identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="0db5b-114">Otherwise, return E\_PROCESS\_CANCELLED\_SWITCH to indicate that the user identity switch should be aborted.</span></span>

## <a name="remarks"></a><span data-ttu-id="0db5b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0db5b-115">Remarks</span></span>

<span data-ttu-id="0db5b-116">Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando un usuario solicita que se cambien las identidades.</span><span class="sxs-lookup"><span data-stu-id="0db5b-116">You may implement this method to provide custom behavior for your application when a user requests that identities be switched.</span></span> <span data-ttu-id="0db5b-117">Puede detener el cambio de identidad pendiente devolviendo el valor E \_ proceso \_ cancelado \_ .</span><span class="sxs-lookup"><span data-stu-id="0db5b-117">You can stop the pending identity switch by returning the value E\_PROCESS\_CANCELLED\_SWITCH.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db5b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0db5b-118">Requirements</span></span>



| <span data-ttu-id="0db5b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db5b-119">Requirement</span></span> | <span data-ttu-id="0db5b-120">Value</span><span class="sxs-lookup"><span data-stu-id="0db5b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db5b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db5b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0db5b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0db5b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0db5b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0db5b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0db5b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0db5b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0db5b-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0db5b-125">End of client support</span></span><br/>    | <span data-ttu-id="0db5b-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0db5b-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="0db5b-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0db5b-127">End of server support</span></span><br/>    | <span data-ttu-id="0db5b-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0db5b-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="0db5b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0db5b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db5b-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db5b-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0db5b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="0db5b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0db5b-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0db5b-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0db5b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0db5b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db5b-134"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db5b-134"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0db5b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0db5b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db5b-136">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="0db5b-136">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="0db5b-137">**IIdentityChangeNotify::SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="0db5b-137">**IIdentityChangeNotify::SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




