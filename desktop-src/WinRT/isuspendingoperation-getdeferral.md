---
description: Solicita que se retrase la operación de suspensión de la aplicación.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Método ISuspendingOperation:: GetDeferral (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907971"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="d1f95-103">ISuspendingOperation:: GetDeferral (método)</span><span class="sxs-lookup"><span data-stu-id="d1f95-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="d1f95-104">Solicita que se retrase la operación de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d1f95-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1f95-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="d1f95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1f95-107">*aplazamiento* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1f95-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1f95-108">La suspensión de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d1f95-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1f95-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1f95-109">Return value</span></span>

<span data-ttu-id="d1f95-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d1f95-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1f95-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1f95-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1f95-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1f95-112">Requirements</span></span>



| <span data-ttu-id="d1f95-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1f95-113">Requirement</span></span> | <span data-ttu-id="d1f95-114">Value</span><span class="sxs-lookup"><span data-stu-id="d1f95-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1f95-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1f95-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d1f95-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1f95-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d1f95-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1f95-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d1f95-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1f95-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d1f95-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1f95-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1f95-120"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1f95-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1f95-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d1f95-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1f95-122"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1f95-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1f95-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1f95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1f95-124">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d1f95-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




