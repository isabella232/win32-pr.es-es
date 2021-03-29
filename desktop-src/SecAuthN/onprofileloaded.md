---
description: Comprueba que se ha cargado el perfil de usuario en línea.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Función OnProfileLoaded (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813603"
---
# <a name="onprofileloaded-function"></a><span data-ttu-id="d1d10-103">OnProfileLoaded función)</span><span class="sxs-lookup"><span data-stu-id="d1d10-103">OnProfileLoaded function</span></span>

<span data-ttu-id="d1d10-104">Comprueba que se ha cargado el perfil de usuario en línea.</span><span class="sxs-lookup"><span data-stu-id="d1d10-104">Checks that the online user profile is loaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1d10-105">Syntax</span></span>


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a><span data-ttu-id="d1d10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d10-107">*ProviderHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1d10-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d10-108">Identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d1d10-108">The provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="d1d10-109">*UserToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1d10-109">*UserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d10-110">Token del usuario cuyo perfil se carga o descarga.</span><span class="sxs-lookup"><span data-stu-id="d1d10-110">Token of the user whose profile is being loaded or unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="d1d10-111">*Cargado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1d10-111">*Loaded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d10-112">**True** si se ha cargado el perfil.</span><span class="sxs-lookup"><span data-stu-id="d1d10-112">**TRUE** if the profile has been loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1d10-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1d10-113">Return value</span></span>

<span data-ttu-id="d1d10-114">Si la función se ejecuta correctamente, la función devuelve el estado \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d1d10-114">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="d1d10-115">Si se produce un error en la función, la función devuelve un código de error distinto de cero que es un error específico del proveedor con fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d1d10-115">If the function fails, the function returns a nonzero error code that is a provider-specific error for diagnostic purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d10-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1d10-116">Remarks</span></span>

<span data-ttu-id="d1d10-117">Se llama a esta función cada vez que se llama a la función [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="d1d10-117">This function is called each time the [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) function is called.</span></span> <span data-ttu-id="d1d10-118">No está sincronizado con **LoadUserProfile**; es decir, **LoadUserProfile** podría haber devuelto y es posible que se haya descargado el perfil en el momento en que se llamó a la función.</span><span class="sxs-lookup"><span data-stu-id="d1d10-118">It is not synchronized with **LoadUserProfile**; that is, **LoadUserProfile** might have returned and the profile might have been unloaded by the time the function was called.</span></span> <span data-ttu-id="d1d10-119">Esta función se puede llamar más de una vez incluso cuando se ha cargado el perfil.</span><span class="sxs-lookup"><span data-stu-id="d1d10-119">This function can be called more than once even when the profile has been loaded.</span></span> <span data-ttu-id="d1d10-120">El proveedor de identidades no debe suponer que una llamada a esta función con la *carga* igual a true irá seguida de una llamada con el valor de *cargado* igual a false.</span><span class="sxs-lookup"><span data-stu-id="d1d10-120">The identity provider must not assume that a call to this function with *Loaded* equal to TRUE will be followed by a call with *Loaded* equal to FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d10-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d10-121">Requirements</span></span>



| <span data-ttu-id="d1d10-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d10-122">Requirement</span></span> | <span data-ttu-id="d1d10-123">Value</span><span class="sxs-lookup"><span data-stu-id="d1d10-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d10-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d10-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d10-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1d10-125">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1d10-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d10-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d10-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1d10-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d1d10-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1d10-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d10-129"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d10-129"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

 
