---
description: Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicación retrasada.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation::D propiedad eadline (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001149"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="363d9-103">ISuspendingOperation::D propiedad eadline</span><span class="sxs-lookup"><span data-stu-id="363d9-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="363d9-104">Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicación retrasada.</span><span class="sxs-lookup"><span data-stu-id="363d9-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="363d9-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="363d9-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="363d9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="363d9-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="363d9-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="363d9-107">Property value</span></span>

<span data-ttu-id="363d9-108">El tiempo restante antes de que continúe una operación de suspensión de aplicación retrasada.</span><span class="sxs-lookup"><span data-stu-id="363d9-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="363d9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="363d9-109">Requirements</span></span>



| <span data-ttu-id="363d9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="363d9-110">Requirement</span></span> | <span data-ttu-id="363d9-111">Value</span><span class="sxs-lookup"><span data-stu-id="363d9-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="363d9-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="363d9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="363d9-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="363d9-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="363d9-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="363d9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="363d9-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="363d9-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="363d9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="363d9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="363d9-117"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="363d9-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="363d9-118">IDL</span><span class="sxs-lookup"><span data-stu-id="363d9-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="363d9-119"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="363d9-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363d9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="363d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363d9-121">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="363d9-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




