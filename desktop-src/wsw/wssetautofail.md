---
title: Función WsSetAutoFail (WebServicesDebug. h)
description: Establece el siguiente punto para insertar un error. Se trata de una función de solo depuración.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servicios Web de la función WsSetAutoFail para Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534924"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="33589-105">WsSetAutoFail función)</span><span class="sxs-lookup"><span data-stu-id="33589-105">WsSetAutoFail function</span></span>

<span data-ttu-id="33589-106">Establece el siguiente punto para insertar un error.</span><span class="sxs-lookup"><span data-stu-id="33589-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="33589-107">Se trata de una función de solo depuración.</span><span class="sxs-lookup"><span data-stu-id="33589-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="33589-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33589-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="33589-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33589-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33589-110">*recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33589-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33589-111">Especifica cuántas operaciones antes de que se produzcan errores.</span><span class="sxs-lookup"><span data-stu-id="33589-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="33589-112">*error* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="33589-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="33589-113">Un puntero a un objeto de [ \_ error de WS](ws-error.md) en el que se debe almacenar información adicional sobre el error si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="33589-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33589-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33589-114">Return value</span></span>

<span data-ttu-id="33589-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="33589-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33589-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33589-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33589-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33589-117">Requirements</span></span>



| <span data-ttu-id="33589-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="33589-118">Requirement</span></span> | <span data-ttu-id="33589-119">Value</span><span class="sxs-lookup"><span data-stu-id="33589-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33589-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33589-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33589-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="33589-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33589-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33589-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33589-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33589-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="33589-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33589-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33589-125"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="33589-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





