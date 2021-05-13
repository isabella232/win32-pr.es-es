---
description: Establece u obtiene el límite de cuota actual del usuario.
title: Propiedad DIDiskQuotaUser.QuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841636"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="de1aa-103">Propiedad DIDiskQuotaUser.QuotaLimit</span><span class="sxs-lookup"><span data-stu-id="de1aa-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="de1aa-104">Establece u obtiene el límite de cuota actual [**del usuario.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="de1aa-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="de1aa-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="de1aa-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1aa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de1aa-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="de1aa-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de1aa-107">Property value</span></span>

<span data-ttu-id="de1aa-108">Valor **entero** que especifica o recibe el límite de cuota actual del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="de1aa-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1aa-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de1aa-109">Requirements</span></span>



| <span data-ttu-id="de1aa-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="de1aa-110">Requirement</span></span> | <span data-ttu-id="de1aa-111">Value</span><span class="sxs-lookup"><span data-stu-id="de1aa-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1aa-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de1aa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="de1aa-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="de1aa-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de1aa-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de1aa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="de1aa-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de1aa-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="de1aa-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de1aa-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de1aa-117"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="de1aa-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1aa-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de1aa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1aa-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="de1aa-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="de1aa-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="de1aa-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="de1aa-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="de1aa-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




