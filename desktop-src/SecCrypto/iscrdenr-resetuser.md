---
description: Borra el nombre de usuario del control de tarjeta inteligente.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'ISCrdEnr:: resetuser (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669656"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="342ca-103">ISCrdEnr:: resetuser (método)</span><span class="sxs-lookup"><span data-stu-id="342ca-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="342ca-104">El método **resetuser** borra el nombre de usuario del control de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="342ca-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="342ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="342ca-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="342ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="342ca-106">Parameters</span></span>

<span data-ttu-id="342ca-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="342ca-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="342ca-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="342ca-108">Remarks</span></span>

<span data-ttu-id="342ca-109">Este método borra cualquier nombre de usuario existente y el certificado inscrito previamente de la memoria.</span><span class="sxs-lookup"><span data-stu-id="342ca-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="342ca-110">No obstante, el certificado inscrito previamente no se quita de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="342ca-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="342ca-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="342ca-111">Requirements</span></span>



| <span data-ttu-id="342ca-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="342ca-112">Requirement</span></span> | <span data-ttu-id="342ca-113">Value</span><span class="sxs-lookup"><span data-stu-id="342ca-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="342ca-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="342ca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="342ca-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="342ca-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="342ca-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="342ca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="342ca-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="342ca-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="342ca-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="342ca-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="342ca-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="342ca-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="342ca-120">IID</span><span class="sxs-lookup"><span data-stu-id="342ca-120">IID</span></span><br/>                      | <span data-ttu-id="342ca-121">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="342ca-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="342ca-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="342ca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342ca-123">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="342ca-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="342ca-124">**ISCrdEnr:: getUserName**</span><span class="sxs-lookup"><span data-stu-id="342ca-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="342ca-125">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="342ca-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="342ca-126">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="342ca-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




