---
title: Función RasAdminGetErrorString (rassapi. h)
description: La función RasAdminGetErrorString recupera una cadena de mensaje que corresponde a un código de error de RAS devuelto por una de las funciones de administración del servidor RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString función RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653605"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="8583f-104">RasAdminGetErrorString función)</span><span class="sxs-lookup"><span data-stu-id="8583f-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="8583f-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="8583f-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="8583f-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8583f-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="8583f-107">Las aplicaciones deben usar la función [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]</span><span class="sxs-lookup"><span data-stu-id="8583f-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="8583f-108">La función **RasAdminGetErrorString** recupera una cadena de mensaje que corresponde a un código de error de Ras devuelto por una de las funciones de administración del servidor RAS (RasAdmin).</span><span class="sxs-lookup"><span data-stu-id="8583f-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="8583f-109">Estas cadenas de mensaje se recuperan de la Rasmsg.dll que se instala como parte de RAS.</span><span class="sxs-lookup"><span data-stu-id="8583f-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="8583f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8583f-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="8583f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8583f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8583f-112">*ResourceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8583f-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8583f-113">Especifica un código de error devuelto por una de las funciones de RasAdmin.</span><span class="sxs-lookup"><span data-stu-id="8583f-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="8583f-114">Este valor debe estar en el intervalo de códigos de error de RASBASE a RASBASEEND.</span><span class="sxs-lookup"><span data-stu-id="8583f-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="8583f-115">Se definen en Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="8583f-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="8583f-116">*lpszString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8583f-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8583f-117">Puntero a un búfer que recibe el mensaje de error correspondiente al código de error especificado.</span><span class="sxs-lookup"><span data-stu-id="8583f-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="8583f-118">*InBufSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8583f-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8583f-119">Especifica el tamaño, en caracteres, del búfer de *lpszString* .</span><span class="sxs-lookup"><span data-stu-id="8583f-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="8583f-120">Los mensajes de error suelen ser de 80 caracteres o menos; un tamaño de búfer de 512 caracteres siempre es adecuado.</span><span class="sxs-lookup"><span data-stu-id="8583f-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8583f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8583f-121">Return value</span></span>

<span data-ttu-id="8583f-122">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8583f-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8583f-123">Si se produce un error en la función, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="8583f-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="8583f-124">Este valor puede ser el último valor de error establecido por las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)o [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) ; o puede ser uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="8583f-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="8583f-125">Value</span><span class="sxs-lookup"><span data-stu-id="8583f-125">Value</span></span>                                                                                                      | <span data-ttu-id="8583f-126">Significado</span><span class="sxs-lookup"><span data-stu-id="8583f-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8583f-127"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="8583f-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="8583f-128">Los parámetros *ResourceId* o *lpszString* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="8583f-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="8583f-129"><dt>**ERROR \_ de \_ búfer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="8583f-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="8583f-130">El tamaño especificado por el parámetro *InBufSize* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="8583f-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="8583f-131">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="8583f-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="8583f-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8583f-132">Remarks</span></span>

<span data-ttu-id="8583f-133">Las funciones RasAdmin pueden devolver códigos de error que no están en el intervalo admitido por la función **RasAdminGetErrorString** .</span><span class="sxs-lookup"><span data-stu-id="8583f-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="8583f-134">Por ejemplo, las funciones RasAdmin pueden devolver códigos de error que se definen en Lmerr. h y Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="8583f-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="8583f-135">Antes de llamar a **RasAdminGetErrorString**, compruebe que el código de error está en el intervalo RASBASE a RASBASEEND, tal y como se define en Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="8583f-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="8583f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8583f-136">Requirements</span></span>



| <span data-ttu-id="8583f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8583f-137">Requirement</span></span> | <span data-ttu-id="8583f-138">Value</span><span class="sxs-lookup"><span data-stu-id="8583f-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8583f-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8583f-139">End of client support</span></span><br/> | <span data-ttu-id="8583f-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8583f-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="8583f-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8583f-141">End of server support</span></span><br/> | <span data-ttu-id="8583f-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8583f-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="8583f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8583f-143">Header</span></span><br/>                | <dl> <span data-ttu-id="8583f-144"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8583f-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="8583f-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8583f-145">Library</span></span><br/>               | <dl> <span data-ttu-id="8583f-146"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8583f-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8583f-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8583f-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8583f-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8583f-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8583f-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8583f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8583f-150">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="8583f-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="8583f-151">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8583f-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="8583f-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="8583f-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="8583f-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="8583f-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="8583f-154">**Fall**</span><span class="sxs-lookup"><span data-stu-id="8583f-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

