---
description: La función GetCaptureTimeStamp devuelve la fecha y la hora en que la captura comenzó a grabar fotogramas.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Función GetCaptureTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540211"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="afb1d-103">GetCaptureTimeStamp función)</span><span class="sxs-lookup"><span data-stu-id="afb1d-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="afb1d-104">La función **GetCaptureTimeStamp** devuelve la fecha y la hora en que la captura comenzó a grabar fotogramas.</span><span class="sxs-lookup"><span data-stu-id="afb1d-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="afb1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afb1d-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="afb1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afb1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb1d-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afb1d-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afb1d-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="afb1d-108">Handle to the capture.</span></span> <span data-ttu-id="afb1d-109">Para obtener información acerca de cómo obtener el identificador de captura, vea la sección Comentarios de este tema **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="afb1d-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb1d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afb1d-110">Return value</span></span>

<span data-ttu-id="afb1d-111">Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="afb1d-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="afb1d-112">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="afb1d-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="afb1d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afb1d-113">Remarks</span></span>

<span data-ttu-id="afb1d-114">La función **GetCaptureTimeStamp** devuelve la hora en que el proveedor de paquetes de red (NPP) comienza a recopilar datos, no cuando el experto carga la captura para su análisis.</span><span class="sxs-lookup"><span data-stu-id="afb1d-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="afb1d-115">No sobrescriba los datos en la estructura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="afb1d-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="afb1d-116">Los datos forman parte de la captura.</span><span class="sxs-lookup"><span data-stu-id="afb1d-116">The data is part of the capture.</span></span> <span data-ttu-id="afb1d-117">Al intentar modificar los datos, se produce una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="afb1d-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="afb1d-118">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="afb1d-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb1d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afb1d-119">Requirements</span></span>



| <span data-ttu-id="afb1d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="afb1d-120">Requirement</span></span> | <span data-ttu-id="afb1d-121">Value</span><span class="sxs-lookup"><span data-stu-id="afb1d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="afb1d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afb1d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="afb1d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="afb1d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="afb1d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afb1d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="afb1d-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afb1d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="afb1d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afb1d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="afb1d-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="afb1d-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="afb1d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afb1d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="afb1d-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afb1d-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="afb1d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afb1d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afb1d-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afb1d-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afb1d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="afb1d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb1d-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="afb1d-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

