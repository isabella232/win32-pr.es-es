---
description: La función ModifyFrame modifica un marco existente con nuevos datos.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Función ModifyFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666543"
---
# <a name="modifyframe-function"></a><span data-ttu-id="b1113-103">ModifyFrame función)</span><span class="sxs-lookup"><span data-stu-id="b1113-103">ModifyFrame function</span></span>

<span data-ttu-id="b1113-104">La función **ModifyFrame** modifica un marco existente con nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="b1113-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1113-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1113-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="b1113-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1113-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1113-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1113-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="b1113-108">Handle to the capture.</span></span> <span data-ttu-id="b1113-109">Para obtener información acerca de cómo obtener el identificador de captura, vea la sección Comentarios de este tema **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="b1113-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="b1113-110">*Númeromarco* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1113-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1113-111">Número de índice del marco.</span><span class="sxs-lookup"><span data-stu-id="b1113-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="b1113-112">*FrameData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1113-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1113-113">Puntero a una matriz de bytes que contiene los nuevos datos de marco.</span><span class="sxs-lookup"><span data-stu-id="b1113-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="b1113-114">*FrameLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1113-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1113-115">Longitud de los datos nuevos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b1113-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b1113-116">*Marca* \[ de tiempo enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b1113-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1113-117">Marca de tiempo que indica cuándo se modificó el marco.</span><span class="sxs-lookup"><span data-stu-id="b1113-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1113-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1113-118">Return value</span></span>

<span data-ttu-id="b1113-119">Si la función es correcta, el valor devuelto es un identificador de un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="b1113-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="b1113-120">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="b1113-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1113-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1113-121">Remarks</span></span>

<span data-ttu-id="b1113-122">Si la llamada se realiza correctamente, la función **ModifyFrame** destruye el marco original.</span><span class="sxs-lookup"><span data-stu-id="b1113-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="b1113-123">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="b1113-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1113-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1113-124">Requirements</span></span>



| <span data-ttu-id="b1113-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1113-125">Requirement</span></span> | <span data-ttu-id="b1113-126">Value</span><span class="sxs-lookup"><span data-stu-id="b1113-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1113-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1113-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b1113-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b1113-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b1113-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1113-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b1113-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1113-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1113-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1113-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1113-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1113-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1113-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1113-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1113-134"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1113-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1113-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1113-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1113-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1113-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




