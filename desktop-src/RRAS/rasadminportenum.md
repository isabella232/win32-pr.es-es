---
title: Función RasAdminPortEnum (rassapi. h)
description: La función RasAdminPortEnum enumera todos los puertos en el servidor RAS especificado. Para cada puerto del servidor, la función devuelve la estructura del \_ Puerto ras \_ 0 que contiene información sobre el puerto.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum función RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649804"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="d5ff4-105">RasAdminPortEnum función)</span><span class="sxs-lookup"><span data-stu-id="d5ff4-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="d5ff4-106">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="d5ff4-107">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="d5ff4-108">Las aplicaciones deben usar la función [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]</span><span class="sxs-lookup"><span data-stu-id="d5ff4-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="d5ff4-109">La función **RasAdminPortEnum** enumera todos los puertos en el servidor RAS especificado.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="d5ff4-110">Para cada puerto del servidor, la función devuelve la estructura [**del \_ Puerto ras \_ 0**](ras-port-0-str.md) que contiene información sobre el puerto.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ff4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5ff4-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="d5ff4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5ff4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ff4-113">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5ff4-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff4-114">Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="d5ff4-115">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff4-116">*ppRasPort0* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5ff4-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff4-117">Puntero a una variable que recibe un puntero a un búfer que contiene una matriz de estructuras del [**\_ Puerto \_ 0 de Ras**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ff4-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="d5ff4-118">Cuando la aplicación haya finalizado con la memoria, libere mediante una llamada a la función [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ff4-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d5ff4-119">*pcEntriesRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5ff4-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ff4-120">Puntero a una variable de 16 bits que recibe el número total de estructuras de [**\_ Puerto ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) devueltas en la matriz *ppRasPort0* .</span><span class="sxs-lookup"><span data-stu-id="d5ff4-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ff4-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5ff4-121">Return value</span></span>

<span data-ttu-id="d5ff4-122">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d5ff4-123">Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="d5ff4-124">Value</span><span class="sxs-lookup"><span data-stu-id="d5ff4-124">Value</span></span>                                                                                             | <span data-ttu-id="d5ff4-125">Significado</span><span class="sxs-lookup"><span data-stu-id="d5ff4-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5ff4-126"><dt>**NERR \_ ItemNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff4-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="d5ff4-127">No se pudo enumerar ningún puerto.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-127">No ports could be enumerated.</span></span> <span data-ttu-id="d5ff4-128">Esto puede deberse a que todos los puertos configurados en el servidor se están usando actualmente para el marcado.</span><span class="sxs-lookup"><span data-stu-id="d5ff4-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="d5ff4-129">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d5ff4-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ff4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ff4-130">Requirements</span></span>



| <span data-ttu-id="d5ff4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ff4-131">Requirement</span></span> | <span data-ttu-id="d5ff4-132">Value</span><span class="sxs-lookup"><span data-stu-id="d5ff4-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ff4-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d5ff4-133">End of client support</span></span><br/> | <span data-ttu-id="d5ff4-134">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5ff4-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="d5ff4-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d5ff4-135">End of server support</span></span><br/> | <span data-ttu-id="d5ff4-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5ff4-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="d5ff4-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5ff4-137">Header</span></span><br/>                | <dl> <span data-ttu-id="d5ff4-138"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff4-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5ff4-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5ff4-139">Library</span></span><br/>               | <dl> <span data-ttu-id="d5ff4-140"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff4-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5ff4-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5ff4-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d5ff4-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5ff4-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ff4-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ff4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ff4-144">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="d5ff4-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d5ff4-145">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="d5ff4-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="d5ff4-146">**\_Puerto ras \_ 0**</span><span class="sxs-lookup"><span data-stu-id="d5ff4-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="d5ff4-147">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5ff4-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

