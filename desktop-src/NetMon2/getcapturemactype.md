---
description: La función GetCaptureMacType devuelve el tipo MAC de una captura determinada.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Función GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808720"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="a654a-103">GetCaptureMacType función)</span><span class="sxs-lookup"><span data-stu-id="a654a-103">GetCaptureMacType function</span></span>

<span data-ttu-id="a654a-104">La función **GetCaptureMacType** devuelve el tipo Mac de una captura determinada.</span><span class="sxs-lookup"><span data-stu-id="a654a-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a654a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a654a-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="a654a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a654a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a654a-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a654a-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a654a-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="a654a-108">Handle to the capture.</span></span> <span data-ttu-id="a654a-109">Para obtener información sobre cómo obtener el identificador de captura, vea la sección Comentarios de este tema **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="a654a-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a654a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a654a-110">Return value</span></span>

<span data-ttu-id="a654a-111">Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de MAC.</span><span class="sxs-lookup"><span data-stu-id="a654a-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="a654a-112">tipo de MAC \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="a654a-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="a654a-113">\_Ethernet de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="a654a-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="a654a-114">\_TOKENRING de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="a654a-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="a654a-115">\_FDDI de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="a654a-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="a654a-116">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="a654a-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="a654a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a654a-117">Return code</span></span>                                                                                              | <span data-ttu-id="a654a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a654a-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="a654a-119"><dt>**\_tipo de Mac NMERR \_ \_ desconocido**</dt></span><span class="sxs-lookup"><span data-stu-id="a654a-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="a654a-120">Monitor de red no encontró un tipo de MAC conocido.</span><span class="sxs-lookup"><span data-stu-id="a654a-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a654a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a654a-121">Remarks</span></span>

<span data-ttu-id="a654a-122">El identificador de la captura se puede obtener de varias maneras, en función de quién realice la llamada.</span><span class="sxs-lookup"><span data-stu-id="a654a-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="a654a-123">En el caso de los expertos, el identificador se especifica en el miembro **hCapture** de la estructura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a654a-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="a654a-124">En el caso de los analizadores, el identificador de captura se puede obtener llamando a la función [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="a654a-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="a654a-125">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="a654a-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a654a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a654a-126">Requirements</span></span>



| <span data-ttu-id="a654a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a654a-127">Requirement</span></span> | <span data-ttu-id="a654a-128">Value</span><span class="sxs-lookup"><span data-stu-id="a654a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a654a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a654a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a654a-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a654a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a654a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a654a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a654a-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a654a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a654a-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a654a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a654a-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a654a-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a654a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a654a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="a654a-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a654a-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a654a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a654a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a654a-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a654a-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




