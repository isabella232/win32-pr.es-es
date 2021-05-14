---
description: Obtiene el uso actual del disco del usuario, en bytes.
title: DiDiskQuotaUser.QuotaUsed, propiedad
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
ms.openlocfilehash: a08d7579ad4de51fbc88b7091f2f906ace838883
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841576"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="38820-103">DiDiskQuotaUser.QuotaUsed, propiedad</span><span class="sxs-lookup"><span data-stu-id="38820-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="38820-104">Obtiene el uso actual del disco del usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="38820-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="38820-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="38820-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38820-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38820-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="38820-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="38820-107">Property value</span></span>

<span data-ttu-id="38820-108">Valor **entero** que se establece en la cantidad de espacio en disco actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="38820-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="38820-109">Si la compresión de archivos NTFS está habilitada, **QuotaUsed** refleja la cantidad de espacio en disco que los datos requerirían en un estado sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="38820-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="38820-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38820-110">Requirements</span></span>



| <span data-ttu-id="38820-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="38820-111">Requirement</span></span> | <span data-ttu-id="38820-112">Value</span><span class="sxs-lookup"><span data-stu-id="38820-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38820-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38820-113">Minimum supported client</span></span><br/> | <span data-ttu-id="38820-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="38820-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38820-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38820-115">Minimum supported server</span></span><br/> | <span data-ttu-id="38820-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38820-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="38820-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38820-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38820-118"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="38820-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38820-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38820-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38820-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="38820-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="38820-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="38820-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="38820-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="38820-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="38820-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="38820-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




