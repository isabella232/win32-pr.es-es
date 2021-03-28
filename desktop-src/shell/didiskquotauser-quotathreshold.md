---
description: Establece u obtiene el umbral de advertencia del usuario, en bytes.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Propiedad DIDiskQuotaUser. QuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907723"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="49737-103">Propiedad DIDiskQuotaUser. QuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="49737-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="49737-104">Establece u obtiene el umbral de advertencia del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="49737-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="49737-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="49737-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="49737-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49737-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="49737-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="49737-107">Property value</span></span>

<span data-ttu-id="49737-108">Valor **entero** que especifica o recibe el umbral de advertencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="49737-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="49737-109">Si el uso de disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **true**, el sistema genera una entrada en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="49737-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="49737-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49737-110">Requirements</span></span>



| <span data-ttu-id="49737-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="49737-111">Requirement</span></span> | <span data-ttu-id="49737-112">Value</span><span class="sxs-lookup"><span data-stu-id="49737-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49737-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49737-113">Minimum supported client</span></span><br/> | <span data-ttu-id="49737-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="49737-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49737-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49737-115">Minimum supported server</span></span><br/> | <span data-ttu-id="49737-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49737-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="49737-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49737-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49737-118"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="49737-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49737-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="49737-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49737-120">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="49737-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="49737-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="49737-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="49737-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="49737-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="49737-123">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="49737-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




