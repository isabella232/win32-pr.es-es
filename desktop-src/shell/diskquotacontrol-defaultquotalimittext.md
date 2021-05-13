---
description: Obtiene el límite de cuota predeterminado como una cadena de texto.
title: Propiedad DiskQuotaControl.DefaultQuotaLimitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841546"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="d992d-103">Propiedad DiskQuotaControl.DefaultQuotaLimitText</span><span class="sxs-lookup"><span data-stu-id="d992d-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="d992d-104">Obtiene el límite de cuota predeterminado como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="d992d-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="d992d-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d992d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d992d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d992d-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="d992d-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d992d-107">Property value</span></span>

<span data-ttu-id="d992d-108">Valor de cadena que contiene el límite de cuota predeterminado para los nuevos usuarios del volumen.</span><span class="sxs-lookup"><span data-stu-id="d992d-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="d992d-109">Por ejemplo, si la cuota predeterminada es de 10,5 MB, el valor de la propiedad es "10,5 MB".</span><span class="sxs-lookup"><span data-stu-id="d992d-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="d992d-110">Si el volumen no tiene ninguna cuota predeterminada, la propiedad se establece en "Sin límite" o en el equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="d992d-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d992d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d992d-111">Requirements</span></span>



| <span data-ttu-id="d992d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d992d-112">Requirement</span></span> | <span data-ttu-id="d992d-113">Value</span><span class="sxs-lookup"><span data-stu-id="d992d-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d992d-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d992d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d992d-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d992d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d992d-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d992d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d992d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d992d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d992d-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d992d-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d992d-119"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d992d-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d992d-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d992d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d992d-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d992d-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="d992d-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="d992d-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




