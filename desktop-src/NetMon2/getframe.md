---
description: La función GetFrame devuelve un identificador a un marco determinado dentro de una captura.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: GetFrame (función) (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153858"
---
# <a name="getframe-function"></a><span data-ttu-id="d4d80-103">GetFrame (función)</span><span class="sxs-lookup"><span data-stu-id="d4d80-103">GetFrame function</span></span>

<span data-ttu-id="d4d80-104">La función **GetFrame** devuelve un identificador a un marco determinado dentro de una captura.</span><span class="sxs-lookup"><span data-stu-id="d4d80-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d80-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4d80-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="d4d80-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4d80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d80-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4d80-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d80-108">Identificador de una captura.</span><span class="sxs-lookup"><span data-stu-id="d4d80-108">Handle to a capture.</span></span> <span data-ttu-id="d4d80-109">Para obtener el identificador de captura, llame a la función [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d80-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d4d80-110">*Númeromarco* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d4d80-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d80-111">Número (basado en cero) del marco.</span><span class="sxs-lookup"><span data-stu-id="d4d80-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="d4d80-112">El número del primer fotograma de una captura es cero.</span><span class="sxs-lookup"><span data-stu-id="d4d80-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d80-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4d80-113">Return value</span></span>

<span data-ttu-id="d4d80-114">Si la función se realiza correctamente, el valor devuelto es un identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="d4d80-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="d4d80-115">Si la función no es correcta (es decir, si *hCapture* no es válida o el número de marco está fuera del intervalo), el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="d4d80-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d80-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4d80-116">Remarks</span></span>

<span data-ttu-id="d4d80-117">Utilice la función **GetFrame** para obtener el identificador de marco necesario al buscar instancias de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4d80-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="d4d80-118">Las funciones que se usan para buscar instancias de propiedad son [FindPropertyInstance](findpropertyinstance.md) , que localiza la primera instancia y [FindPropertyInstanceRestart](findpropertyinstancerestart.md) , que busca la instancia siguiente.</span><span class="sxs-lookup"><span data-stu-id="d4d80-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="d4d80-119">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrame** .</span><span class="sxs-lookup"><span data-stu-id="d4d80-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d80-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d80-120">Requirements</span></span>



| <span data-ttu-id="d4d80-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d80-121">Requirement</span></span> | <span data-ttu-id="d4d80-122">Value</span><span class="sxs-lookup"><span data-stu-id="d4d80-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d80-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d80-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d80-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4d80-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d4d80-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d80-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d80-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d4d80-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4d80-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4d80-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d80-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d80-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d4d80-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d4d80-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4d80-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4d80-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4d80-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4d80-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d80-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d80-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d80-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4d80-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d80-134">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="d4d80-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="d4d80-135">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="d4d80-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




