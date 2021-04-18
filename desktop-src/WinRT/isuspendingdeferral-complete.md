---
description: Notifica al sistema que la aplicación ha guardado sus datos y está listo para su suspensión.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Método ISuspendingDeferral:: Complete (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715151"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="2f127-103">ISuspendingDeferral:: Complete (método)</span><span class="sxs-lookup"><span data-stu-id="2f127-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="2f127-104">Notifica al sistema que la aplicación ha guardado sus datos y está listo para su suspensión.</span><span class="sxs-lookup"><span data-stu-id="2f127-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f127-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f127-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="2f127-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f127-106">Parameters</span></span>

<span data-ttu-id="2f127-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2f127-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f127-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f127-108">Return value</span></span>

<span data-ttu-id="2f127-109">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="2f127-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f127-110">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f127-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f127-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f127-111">Requirements</span></span>



| <span data-ttu-id="2f127-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f127-112">Requirement</span></span> | <span data-ttu-id="2f127-113">Value</span><span class="sxs-lookup"><span data-stu-id="2f127-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f127-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f127-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2f127-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f127-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2f127-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f127-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2f127-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f127-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2f127-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f127-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f127-119"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f127-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f127-120">IDL</span><span class="sxs-lookup"><span data-stu-id="2f127-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f127-121"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f127-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f127-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f127-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f127-123">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="2f127-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




