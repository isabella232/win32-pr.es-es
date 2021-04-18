---
title: Función RasAdminFreeBuffer (rassapi. h)
description: La función RasAdminFreeBuffer libera la memoria asignada por RAS en nombre del autor de la llamada.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RasAdminFreeBuffer función RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681303"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="ea643-104">RasAdminFreeBuffer función)</span><span class="sxs-lookup"><span data-stu-id="ea643-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="ea643-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="ea643-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="ea643-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ea643-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="ea643-107">Las aplicaciones deben usar la función [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]</span><span class="sxs-lookup"><span data-stu-id="ea643-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="ea643-108">La función **RasAdminFreeBuffer** libera la memoria asignada por ras en nombre del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ea643-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea643-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea643-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="ea643-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea643-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea643-111">*Puntero* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea643-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea643-112">Puntero al búfer que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="ea643-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea643-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea643-113">Return value</span></span>

<span data-ttu-id="ea643-114">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ea643-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ea643-115">Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="ea643-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="ea643-116">Value</span><span class="sxs-lookup"><span data-stu-id="ea643-116">Value</span></span>                                                                                                    | <span data-ttu-id="ea643-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ea643-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ea643-118"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="ea643-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="ea643-119">El parámetro de *puntero* no es válido.</span><span class="sxs-lookup"><span data-stu-id="ea643-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="ea643-120">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ea643-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea643-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea643-121">Remarks</span></span>

<span data-ttu-id="ea643-122">Use la función **RasAdminFreeBuffer** para liberar los búferes asignados por las funciones [**RasAdminPortEnum**](rasadminportenum.md) y [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ea643-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea643-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea643-123">Requirements</span></span>



| <span data-ttu-id="ea643-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea643-124">Requirement</span></span> | <span data-ttu-id="ea643-125">Value</span><span class="sxs-lookup"><span data-stu-id="ea643-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea643-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ea643-126">End of client support</span></span><br/> | <span data-ttu-id="ea643-127">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea643-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="ea643-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ea643-128">End of server support</span></span><br/> | <span data-ttu-id="ea643-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea643-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="ea643-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea643-130">Header</span></span><br/>                | <dl> <span data-ttu-id="ea643-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea643-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea643-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea643-132">Library</span></span><br/>               | <dl> <span data-ttu-id="ea643-133"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea643-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea643-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea643-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ea643-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea643-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea643-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea643-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea643-137">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="ea643-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="ea643-138">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="ea643-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="ea643-139">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="ea643-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="ea643-140">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="ea643-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

