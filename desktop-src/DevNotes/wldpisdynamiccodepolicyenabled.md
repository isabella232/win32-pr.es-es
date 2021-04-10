---
description: Recupera un valor que describe el estado de aplicación de la Directiva de Device Guard para código dinámico de .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Función WldpIsDynamicCodePolicyEnabled (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152780"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="3d98a-103">WldpIsDynamicCodePolicyEnabled función)</span><span class="sxs-lookup"><span data-stu-id="3d98a-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="3d98a-104">Recupera un valor que describe el estado de aplicación de la Directiva de Device Guard para código dinámico de .NET.</span><span class="sxs-lookup"><span data-stu-id="3d98a-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d98a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d98a-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="3d98a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d98a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d98a-107">*IsEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3d98a-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d98a-108">Si se ejecuta correctamente, devuelve **true** si la Directiva de Device Guard aplica la Directiva de código dinámico .net; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="3d98a-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d98a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d98a-109">Return value</span></span>

<span data-ttu-id="3d98a-110">Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3d98a-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d98a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d98a-111">Remarks</span></span>

<span data-ttu-id="3d98a-112">El código dinámico hace referencia al código generado dinámicamente de la CRL de .NET.</span><span class="sxs-lookup"><span data-stu-id="3d98a-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d98a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d98a-113">Requirements</span></span>



| <span data-ttu-id="3d98a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d98a-114">Requirement</span></span> | <span data-ttu-id="3d98a-115">Value</span><span class="sxs-lookup"><span data-stu-id="3d98a-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d98a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d98a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d98a-117">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d98a-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3d98a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d98a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d98a-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d98a-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d98a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d98a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d98a-121"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d98a-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d98a-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d98a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d98a-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d98a-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




