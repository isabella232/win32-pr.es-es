---
title: Función RasAdminPortClearStatistics (rassapi. h)
description: La función RasAdminPortClearStatistics restablece los contadores que representan las diversas estadísticas indicadas por la función RasAdminPortGetInfo en la \_ estructura de estadísticas del puerto ras \_ . Los contadores se restablecen a cero y comienzan a acumularse.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics función RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649805"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="53a5d-105">RasAdminPortClearStatistics función)</span><span class="sxs-lookup"><span data-stu-id="53a5d-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="53a5d-106">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="53a5d-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="53a5d-107">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53a5d-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="53a5d-108">Las aplicaciones deben usar la función [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]</span><span class="sxs-lookup"><span data-stu-id="53a5d-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="53a5d-109">La función **RasAdminPortClearStatistics** restablece los contadores que representan las diversas estadísticas indicadas por la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) en la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) .</span><span class="sxs-lookup"><span data-stu-id="53a5d-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="53a5d-110">Los contadores se restablecen a cero y comienzan a acumularse.</span><span class="sxs-lookup"><span data-stu-id="53a5d-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a5d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53a5d-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="53a5d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53a5d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a5d-113">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53a5d-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a5d-114">Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="53a5d-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="53a5d-115">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="53a5d-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="53a5d-116">*lpszPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53a5d-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a5d-117">Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="53a5d-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a5d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53a5d-118">Return value</span></span>

<span data-ttu-id="53a5d-119">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="53a5d-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="53a5d-120">Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="53a5d-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="53a5d-121">Value</span><span class="sxs-lookup"><span data-stu-id="53a5d-121">Value</span></span>                                                                                                 | <span data-ttu-id="53a5d-122">Significado</span><span class="sxs-lookup"><span data-stu-id="53a5d-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="53a5d-123"><dt>**\_ \_ no existe el desarrollador de errores \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53a5d-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="53a5d-124">El puerto especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="53a5d-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="53a5d-125">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="53a5d-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="53a5d-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53a5d-126">Remarks</span></span>

<span data-ttu-id="53a5d-127">La función **RasAdminPortClearStatistics** borra las estadísticas del servidor, no localmente dentro de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="53a5d-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="53a5d-128">Esto significa que las estadísticas también se restablecen para cualquier otra aplicación que esté supervisando el puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="53a5d-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="53a5d-129">Si el puerto *lpszPort* forma parte de una conexión Multilink, **RasAdminPortClearStatistics** restablece las estadísticas para el puerto especificado, la función también restablece las estadísticas acumuladas de la conexión multivínculo.</span><span class="sxs-lookup"><span data-stu-id="53a5d-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="53a5d-130">Sin embargo, la función no afecta a las estadísticas individuales de otros puertos que forman parte de la conexión de multivínculo.</span><span class="sxs-lookup"><span data-stu-id="53a5d-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a5d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53a5d-131">Requirements</span></span>



| <span data-ttu-id="53a5d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a5d-132">Requirement</span></span> | <span data-ttu-id="53a5d-133">Value</span><span class="sxs-lookup"><span data-stu-id="53a5d-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53a5d-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="53a5d-134">End of client support</span></span><br/> | <span data-ttu-id="53a5d-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53a5d-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="53a5d-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="53a5d-136">End of server support</span></span><br/> | <span data-ttu-id="53a5d-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53a5d-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="53a5d-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53a5d-138">Header</span></span><br/>                | <dl> <span data-ttu-id="53a5d-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a5d-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="53a5d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53a5d-140">Library</span></span><br/>               | <dl> <span data-ttu-id="53a5d-141"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53a5d-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="53a5d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53a5d-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="53a5d-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a5d-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a5d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a5d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a5d-145">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="53a5d-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="53a5d-146">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="53a5d-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="53a5d-147">**\_estadísticas de Puerto ras \_**</span><span class="sxs-lookup"><span data-stu-id="53a5d-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="53a5d-148">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="53a5d-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

