---
description: Se llama cuando se cambian las identidades de usuario.
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'IIdentityChangeNotify:: SwitchIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 925b52a4470c768501dd928784d85a89d05a90c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997665"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a><span data-ttu-id="59ac8-103">IIdentityChangeNotify:: SwitchIdentities (método)</span><span class="sxs-lookup"><span data-stu-id="59ac8-103">IIdentityChangeNotify::SwitchIdentities method</span></span>

<span data-ttu-id="59ac8-104">\[**SwitchIdentities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="59ac8-104">\[**SwitchIdentities** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="59ac8-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="59ac8-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="59ac8-106">Se llama cuando se cambian las identidades de usuario.</span><span class="sxs-lookup"><span data-stu-id="59ac8-106">Called when user identities are switched.</span></span>

## <a name="syntax"></a><span data-ttu-id="59ac8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59ac8-107">Syntax</span></span>


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a><span data-ttu-id="59ac8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59ac8-108">Parameters</span></span>

<span data-ttu-id="59ac8-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="59ac8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59ac8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59ac8-110">Return value</span></span>

<span data-ttu-id="59ac8-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="59ac8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="59ac8-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="59ac8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59ac8-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59ac8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ac8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59ac8-114">Remarks</span></span>

<span data-ttu-id="59ac8-115">Puede implementar este método para proporcionar un comportamiento personalizado para la aplicación cuando un usuario ha cambiado correctamente las identidades.</span><span class="sxs-lookup"><span data-stu-id="59ac8-115">You may implement this method to provide custom behavior for your application when a user has successfully switched identities.</span></span> <span data-ttu-id="59ac8-116">Para proporcionar un comportamiento personalizado antes de que se produzca un cambio de identidad de usuario, implemente el método [**IIdentityChangeNotify:: QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) .</span><span class="sxs-lookup"><span data-stu-id="59ac8-116">To provide custom behavior before a user identity switch occurs, implement the [**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ac8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ac8-117">Requirements</span></span>



| <span data-ttu-id="59ac8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ac8-118">Requirement</span></span> | <span data-ttu-id="59ac8-119">Value</span><span class="sxs-lookup"><span data-stu-id="59ac8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59ac8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ac8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59ac8-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59ac8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="59ac8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ac8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59ac8-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59ac8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="59ac8-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="59ac8-124">End of client support</span></span><br/>    | <span data-ttu-id="59ac8-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="59ac8-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="59ac8-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="59ac8-126">End of server support</span></span><br/>    | <span data-ttu-id="59ac8-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="59ac8-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="59ac8-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59ac8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ac8-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ac8-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="59ac8-130">IDL</span><span class="sxs-lookup"><span data-stu-id="59ac8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59ac8-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59ac8-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="59ac8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59ac8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59ac8-133"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59ac8-133"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="59ac8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="59ac8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ac8-135">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="59ac8-135">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> <dt>

[<span data-ttu-id="59ac8-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="59ac8-136">**IIdentityChangeNotify::QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




