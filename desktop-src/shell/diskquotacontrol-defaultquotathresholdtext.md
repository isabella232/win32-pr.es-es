---
description: Obtiene el umbral de cuota predeterminado como una cadena de texto.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Propiedad DiskQuotaControl. DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153907"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="9e597-103">Propiedad DiskQuotaControl. DefaultQuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="9e597-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="9e597-104">Obtiene el umbral de cuota predeterminado como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="9e597-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="9e597-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9e597-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e597-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e597-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="9e597-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9e597-107">Property value</span></span>

<span data-ttu-id="9e597-108">Valor de cadena que contiene el umbral de cuota predeterminado para el volumen.</span><span class="sxs-lookup"><span data-stu-id="9e597-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e597-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e597-109">Remarks</span></span>

<span data-ttu-id="9e597-110">El umbral de cuota predeterminado se aplica automáticamente a los nuevos usuarios del volumen.</span><span class="sxs-lookup"><span data-stu-id="9e597-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="9e597-111">Si el uso de disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **true**, el sistema genera una entrada en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="9e597-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="9e597-112">Por ejemplo, si el umbral predeterminado es 10,0 MB, el valor de la propiedad es "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="9e597-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="9e597-113">Si el volumen no tiene ningún umbral predeterminado, la propiedad se establece en "sin límite" o en el equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="9e597-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e597-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e597-114">Requirements</span></span>



| <span data-ttu-id="9e597-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e597-115">Requirement</span></span> | <span data-ttu-id="9e597-116">Value</span><span class="sxs-lookup"><span data-stu-id="9e597-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e597-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e597-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e597-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9e597-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e597-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e597-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e597-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e597-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9e597-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e597-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e597-122"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9e597-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e597-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e597-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e597-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="9e597-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




