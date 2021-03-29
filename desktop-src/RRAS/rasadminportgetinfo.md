---
title: Función RasAdminPortGetInfo (rassapi. h)
description: La función RasAdminPortGetInfo recupera información acerca de un puerto específico en un servidor especificado.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo función RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680703"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="bca91-104">RasAdminPortGetInfo función)</span><span class="sxs-lookup"><span data-stu-id="bca91-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="bca91-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="bca91-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="bca91-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bca91-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="bca91-107">Las aplicaciones deben usar la función [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="bca91-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="bca91-108">La función **RasAdminPortGetInfo** recupera información acerca de un puerto específico en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="bca91-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca91-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bca91-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="bca91-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bca91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca91-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bca91-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca91-112">Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="bca91-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="bca91-113">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="bca91-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="bca91-114">*lpszPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bca91-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca91-115">Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bca91-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="bca91-116">*pRasPort1* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bca91-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca91-117">Puntero a la estructura del [**Puerto de Ras \_ \_ 1**](ras-port-1-str.md) que la función rellena con información sobre el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="bca91-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="bca91-118">*pRasStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bca91-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca91-119">Puntero a la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) que la función rellena con estadísticas sobre el puerto.</span><span class="sxs-lookup"><span data-stu-id="bca91-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="bca91-120">*ppRasParams* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bca91-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca91-121">Puntero a una variable de puntero que recibe la dirección de una matriz de estructuras de [**\_ parámetros de Ras**](ras-parameters-str.md) .</span><span class="sxs-lookup"><span data-stu-id="bca91-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="bca91-122">Cada estructura contiene el nombre de una clave específica del medio, como MAXCONNECTBPS, y su valor asociado.</span><span class="sxs-lookup"><span data-stu-id="bca91-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="bca91-123">Cuando la aplicación haya finalizado con esta memoria, libere llamando a la función [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bca91-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca91-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bca91-124">Return value</span></span>

<span data-ttu-id="bca91-125">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bca91-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="bca91-126">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="bca91-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="bca91-127">Value</span><span class="sxs-lookup"><span data-stu-id="bca91-127">Value</span></span>                                                                                                     | <span data-ttu-id="bca91-128">Significado</span><span class="sxs-lookup"><span data-stu-id="bca91-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bca91-129"><dt>**\_ \_ no existe el desarrollador de errores \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bca91-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="bca91-130">El puerto especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="bca91-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="bca91-131"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bca91-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="bca91-132">Memoria insuficiente para asignar un búfer para la matriz *ppRasParams* .</span><span class="sxs-lookup"><span data-stu-id="bca91-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="bca91-133">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="bca91-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="bca91-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bca91-134">Requirements</span></span>



| <span data-ttu-id="bca91-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bca91-135">Requirement</span></span> | <span data-ttu-id="bca91-136">Value</span><span class="sxs-lookup"><span data-stu-id="bca91-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bca91-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="bca91-137">End of client support</span></span><br/> | <span data-ttu-id="bca91-138">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bca91-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bca91-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bca91-139">End of server support</span></span><br/> | <span data-ttu-id="bca91-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bca91-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bca91-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bca91-141">Header</span></span><br/>                | <dl> <span data-ttu-id="bca91-142"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bca91-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="bca91-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bca91-143">Library</span></span><br/>               | <dl> <span data-ttu-id="bca91-144"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bca91-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bca91-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bca91-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bca91-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bca91-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bca91-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bca91-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca91-148">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="bca91-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="bca91-149">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="bca91-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="bca91-150">**parámetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="bca91-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="bca91-151">**\_Puerto ras \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bca91-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="bca91-152">**\_estadísticas de Puerto ras \_**</span><span class="sxs-lookup"><span data-stu-id="bca91-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="bca91-153">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="bca91-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

