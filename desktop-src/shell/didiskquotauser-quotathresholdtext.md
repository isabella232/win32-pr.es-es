---
description: Obtiene el umbral de advertencia del usuario como una cadena de texto.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Propiedad DIDiskQuotaUser. QuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984270"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="3520c-103">Propiedad DIDiskQuotaUser. QuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="3520c-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="3520c-104">Obtiene el umbral de advertencia del usuario como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="3520c-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="3520c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3520c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3520c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3520c-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="3520c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3520c-107">Property value</span></span>

<span data-ttu-id="3520c-108">Valor de cadena que contiene el umbral de advertencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="3520c-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="3520c-109">Si el uso de disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **true**, el sistema genera una entrada en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="3520c-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="3520c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3520c-110">Requirements</span></span>



| <span data-ttu-id="3520c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3520c-111">Requirement</span></span> | <span data-ttu-id="3520c-112">Value</span><span class="sxs-lookup"><span data-stu-id="3520c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3520c-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3520c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3520c-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3520c-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3520c-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3520c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3520c-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3520c-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3520c-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3520c-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3520c-118"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3520c-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3520c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3520c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3520c-120">**Objeto IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="3520c-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="3520c-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3520c-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="3520c-122">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="3520c-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="3520c-123">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3520c-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




