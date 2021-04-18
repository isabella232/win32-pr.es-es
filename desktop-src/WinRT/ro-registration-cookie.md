---
description: Representa los generadores de activación que se registran mediante una llamada a la función RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705664"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="d6fad-103">\_cookie de registro de ro \_</span><span class="sxs-lookup"><span data-stu-id="d6fad-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="d6fad-104">Representa los generadores de activación que se registran mediante una llamada a la función [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .</span><span class="sxs-lookup"><span data-stu-id="d6fad-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="d6fad-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6fad-105">Remarks</span></span>

<span data-ttu-id="d6fad-106">La función [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) devuelve una **\_ \_ cookie de registro de ro** cuando se registran generadores de clases activables con el Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="d6fad-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="d6fad-107">La función [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa la cookie para quitar los generadores de clases.</span><span class="sxs-lookup"><span data-stu-id="d6fad-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fad-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6fad-108">Requirements</span></span>



| <span data-ttu-id="d6fad-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6fad-109">Requirement</span></span> | <span data-ttu-id="d6fad-110">Value</span><span class="sxs-lookup"><span data-stu-id="d6fad-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fad-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fad-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fad-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d6fad-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="d6fad-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fad-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fad-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d6fad-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="d6fad-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6fad-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6fad-116"><dt>Roapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6fad-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fad-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6fad-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fad-118">**RoRegisterActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="d6fad-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="d6fad-119">**RoRevokeActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="d6fad-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
