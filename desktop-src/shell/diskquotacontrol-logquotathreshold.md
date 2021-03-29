---
description: Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Propiedad DiskQuotaControl. LogQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984243"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="d9636-103">Propiedad DiskQuotaControl. LogQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="d9636-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="d9636-104">Establece u obtiene un valor booleano que indica si se realizará una entrada del registro de eventos del sistema cuando un usuario supere su umbral de cuota asignado.</span><span class="sxs-lookup"><span data-stu-id="d9636-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="d9636-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d9636-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9636-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9636-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="d9636-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9636-107">Property value</span></span>

<span data-ttu-id="d9636-108">Esta propiedad se establece en **true** si se realiza una entrada del registro de eventos del sistema cuando el usuario supera su umbral de advertencia de cuota o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d9636-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9636-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9636-109">Requirements</span></span>



| <span data-ttu-id="d9636-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9636-110">Requirement</span></span> | <span data-ttu-id="d9636-111">Value</span><span class="sxs-lookup"><span data-stu-id="d9636-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9636-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9636-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d9636-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d9636-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9636-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9636-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d9636-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9636-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d9636-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9636-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9636-117"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d9636-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9636-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9636-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9636-119">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="d9636-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="d9636-120">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="d9636-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="d9636-121">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d9636-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




