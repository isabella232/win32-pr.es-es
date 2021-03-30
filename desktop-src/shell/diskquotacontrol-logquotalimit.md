---
description: Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Propiedad DiskQuotaControl. LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984246"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="fce12-103">Propiedad DiskQuotaControl. LogQuotaLimit</span><span class="sxs-lookup"><span data-stu-id="fce12-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="fce12-104">Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su límite de cuota asignado.</span><span class="sxs-lookup"><span data-stu-id="fce12-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="fce12-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fce12-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce12-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fce12-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="fce12-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fce12-107">Property value</span></span>

<span data-ttu-id="fce12-108">Esta propiedad se establece en **true** si se realiza una entrada del registro de eventos del sistema cuando el usuario supera su límite de cuota, o bien **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fce12-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce12-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce12-109">Requirements</span></span>



| <span data-ttu-id="fce12-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce12-110">Requirement</span></span> | <span data-ttu-id="fce12-111">Value</span><span class="sxs-lookup"><span data-stu-id="fce12-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce12-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fce12-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fce12-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fce12-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fce12-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fce12-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fce12-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fce12-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fce12-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fce12-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce12-117"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fce12-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce12-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fce12-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce12-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="fce12-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="fce12-120">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fce12-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="fce12-121">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="fce12-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




