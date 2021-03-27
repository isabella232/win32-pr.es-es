---
description: Obtiene el uso actual del disco del usuario, en bytes.
title: Propiedad DIDiskQuotaUser. QuotaUsed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153911"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="e04bc-103">Propiedad DIDiskQuotaUser. QuotaUsed</span><span class="sxs-lookup"><span data-stu-id="e04bc-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="e04bc-104">Obtiene el uso actual del disco del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e04bc-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="e04bc-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e04bc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04bc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e04bc-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="e04bc-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e04bc-107">Property value</span></span>

<span data-ttu-id="e04bc-108">Valor **entero** que se establece en la cantidad de espacio en disco que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e04bc-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="e04bc-109">Si está habilitada la compresión de archivos NTFS, **QuotaUsed** refleja la cantidad de espacio en disco que los datos necesitarían en un estado sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="e04bc-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="e04bc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e04bc-110">Requirements</span></span>



| <span data-ttu-id="e04bc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e04bc-111">Requirement</span></span> | <span data-ttu-id="e04bc-112">Value</span><span class="sxs-lookup"><span data-stu-id="e04bc-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04bc-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e04bc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e04bc-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e04bc-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e04bc-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e04bc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e04bc-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e04bc-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e04bc-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e04bc-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e04bc-118"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e04bc-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04bc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e04bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04bc-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="e04bc-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="e04bc-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="e04bc-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="e04bc-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="e04bc-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="e04bc-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="e04bc-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




