---
description: Establece u obtiene el umbral de cuota predeterminado.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Propiedad DiskQuotaControl. DefaultQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984258"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="e5e7b-103">Propiedad DiskQuotaControl. DefaultQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="e5e7b-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="e5e7b-104">Establece u obtiene el umbral de cuota predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="e5e7b-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e7b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5e7b-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="e5e7b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e5e7b-107">Property value</span></span>

<span data-ttu-id="e5e7b-108">Valor **entero** que se establece en el umbral de advertencia predeterminado para los nuevos usuarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e7b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5e7b-109">Remarks</span></span>

<span data-ttu-id="e5e7b-110">El umbral de cuota predeterminado se aplica automáticamente a los nuevos usuarios del volumen.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="e5e7b-111">Si el uso de disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **true**, el sistema genera una entrada en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="e5e7b-112">Por ejemplo, si el umbral predeterminado es 10,0 MB, el valor de la propiedad es "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="e5e7b-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="e5e7b-113">Si el volumen no tiene ningún umbral predeterminado, la propiedad se establece en "sin límite" o en el equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="e5e7b-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e7b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5e7b-114">Requirements</span></span>



| <span data-ttu-id="e5e7b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5e7b-115">Requirement</span></span> | <span data-ttu-id="e5e7b-116">Value</span><span class="sxs-lookup"><span data-stu-id="e5e7b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e7b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5e7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e7b-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5e7b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5e7b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5e7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e7b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5e7b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e5e7b-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5e7b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e7b-122"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e5e7b-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e7b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5e7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e7b-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="e5e7b-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




