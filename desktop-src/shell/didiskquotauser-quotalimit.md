---
description: Establece u obtiene el límite de cuota actual del usuario.
title: Propiedad DIDiskQuotaUser. QuotaLimit
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
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984271"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="f63b4-103">Propiedad DIDiskQuotaUser. QuotaLimit</span><span class="sxs-lookup"><span data-stu-id="f63b4-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="f63b4-104">Establece u obtiene el [**límite de cuota**](diskquotacontrol-object.md)actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="f63b4-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="f63b4-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f63b4-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f63b4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f63b4-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="f63b4-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f63b4-107">Property value</span></span>

<span data-ttu-id="f63b4-108">Valor **entero** que especifica o recibe el límite de cuota actual del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="f63b4-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f63b4-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f63b4-109">Requirements</span></span>



| <span data-ttu-id="f63b4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63b4-110">Requirement</span></span> | <span data-ttu-id="f63b4-111">Value</span><span class="sxs-lookup"><span data-stu-id="f63b4-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63b4-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f63b4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f63b4-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f63b4-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f63b4-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f63b4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f63b4-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f63b4-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f63b4-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f63b4-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f63b4-117"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f63b4-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63b4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f63b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63b4-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="f63b4-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="f63b4-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="f63b4-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="f63b4-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="f63b4-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




