---
description: Inicia la descodificación de un nuevo marco.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Función NtGdiDdBeginMoCompFrame (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538542"
---
# <a name="ntgdiddbeginmocompframe-function"></a><span data-ttu-id="093ed-103">NtGdiDdBeginMoCompFrame función)</span><span class="sxs-lookup"><span data-stu-id="093ed-103">NtGdiDdBeginMoCompFrame function</span></span>

<span data-ttu-id="093ed-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="093ed-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="093ed-105">En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="093ed-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="093ed-106">Inicia la descodificación de un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="093ed-106">Starts decoding a new frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="093ed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="093ed-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="093ed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="093ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093ed-109">*hMoComp* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="093ed-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093ed-110">Identificador de una [**estructura \_ \_ local DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contiene una descripción de la compensación de movimiento que se solicita.</span><span class="sxs-lookup"><span data-stu-id="093ed-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="093ed-111">*puBeginFrameData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="093ed-111">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="093ed-112">Puntero a una estructura [**DD \_ BEGINMOCOMPFRAMEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) que contiene la información necesaria para iniciar la descodificación de un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="093ed-112">Pointer to a [**DD\_BEGINMOCOMPFRAMEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) structure that contains the information needed to start decoding a new frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="093ed-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="093ed-113">Return value</span></span>

<span data-ttu-id="093ed-114">**NtGdiDdBeginMoCompFrame** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="093ed-114">**NtGdiDdBeginMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="093ed-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="093ed-115">Return code</span></span>                                                                                              | <span data-ttu-id="093ed-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="093ed-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="093ed-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="093ed-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="093ed-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="093ed-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="093ed-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="093ed-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="093ed-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="093ed-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="093ed-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="093ed-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="093ed-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="093ed-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="093ed-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="093ed-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="093ed-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="093ed-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="093ed-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="093ed-125">Remarks</span></span>

<span data-ttu-id="093ed-126">Para obtener más información, vea el kit de desarrollo de controladores (DDK) de Microsoft DirectX video Acceleration.</span><span class="sxs-lookup"><span data-stu-id="093ed-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="093ed-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="093ed-127">Requirements</span></span>



| <span data-ttu-id="093ed-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="093ed-128">Requirement</span></span> | <span data-ttu-id="093ed-129">Value</span><span class="sxs-lookup"><span data-stu-id="093ed-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="093ed-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="093ed-130">Minimum supported client</span></span><br/> | <span data-ttu-id="093ed-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="093ed-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="093ed-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="093ed-132">Minimum supported server</span></span><br/> | <span data-ttu-id="093ed-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="093ed-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="093ed-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="093ed-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="093ed-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="093ed-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="093ed-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="093ed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093ed-137">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="093ed-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
