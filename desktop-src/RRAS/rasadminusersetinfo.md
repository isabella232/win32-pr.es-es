---
title: Función RasAdminUserSetInfo (rassapi. h)
description: La función RasAdminUserSetInfo establece los permisos RAS y el número de teléfono de devolución de llamada para un usuario especificado.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo función RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649815"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="455e3-104">RasAdminUserSetInfo función)</span><span class="sxs-lookup"><span data-stu-id="455e3-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="455e3-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="455e3-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="455e3-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="455e3-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="455e3-107">Las aplicaciones deben usar la función [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="455e3-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="455e3-108">La función **RasAdminUserSetInfo** establece los permisos ras y el número de teléfono de devolución de llamada para un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="455e3-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="455e3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="455e3-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="455e3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="455e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455e3-111">*lpszUserAccountServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="455e3-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455e3-112">Puntero a una cadena Unicode terminada en null que especifica el nombre del controlador de dominio principal o de reserva que tiene la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="455e3-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="455e3-113">Use la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener este nombre de servidor.</span><span class="sxs-lookup"><span data-stu-id="455e3-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="455e3-114">*lpszUser* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="455e3-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455e3-115">Puntero a una cadena Unicode terminada en null que especifica el nombre del usuario para el que se va a establecer información de RAS.</span><span class="sxs-lookup"><span data-stu-id="455e3-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="455e3-116">*pRasUser0* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="455e3-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455e3-117">Puntero a la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) que especifica los nuevos datos ras para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="455e3-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="455e3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="455e3-118">Return value</span></span>

<span data-ttu-id="455e3-119">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="455e3-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="455e3-120">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="455e3-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="455e3-121">Value</span><span class="sxs-lookup"><span data-stu-id="455e3-121">Value</span></span>                                                                                                           | <span data-ttu-id="455e3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="455e3-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="455e3-123"><dt>**ERROR de \_ datos no válidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="455e3-124">El búfer *pRasUser0* contiene datos no válidos.</span><span class="sxs-lookup"><span data-stu-id="455e3-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="455e3-125"><dt>**ERROR \_ de \_ número de devolución de llamada no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="455e3-126">El número de devolución de llamada especificado en el búfer *pRasUser0* contiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="455e3-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="455e3-127"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="455e3-128">Memoria insuficiente para realizar esta función.</span><span class="sxs-lookup"><span data-stu-id="455e3-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="455e3-129">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="455e3-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="455e3-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="455e3-130">Remarks</span></span>

<span data-ttu-id="455e3-131">Al establecer los permisos RAS para un usuario, el miembro **bfPrivilege** de la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) debe especificar al menos una de las marcas de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="455e3-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="455e3-132">Por ejemplo, para establecer los privilegios de un usuario para permitir el privilegio de acceso telefónico pero ningún privilegio de devolución de llamada, establezca **bfPrivilege** en RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.</span><span class="sxs-lookup"><span data-stu-id="455e3-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="455e3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="455e3-133">Requirements</span></span>



| <span data-ttu-id="455e3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="455e3-134">Requirement</span></span> | <span data-ttu-id="455e3-135">Value</span><span class="sxs-lookup"><span data-stu-id="455e3-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="455e3-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="455e3-136">End of client support</span></span><br/> | <span data-ttu-id="455e3-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="455e3-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="455e3-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="455e3-138">End of server support</span></span><br/> | <span data-ttu-id="455e3-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="455e3-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="455e3-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="455e3-140">Header</span></span><br/>                | <dl> <span data-ttu-id="455e3-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="455e3-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="455e3-142">Library</span></span><br/>               | <dl> <span data-ttu-id="455e3-143"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="455e3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="455e3-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="455e3-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455e3-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455e3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="455e3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455e3-147">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="455e3-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="455e3-148">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="455e3-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="455e3-149">**Usuario de RAS \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="455e3-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="455e3-150">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="455e3-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="455e3-151">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="455e3-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

