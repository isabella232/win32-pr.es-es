---
title: Función RasAdminUserGetInfo (rassapi. h)
description: La función RasAdminUserGetInfo obtiene la información de los permisos RAS y del número de teléfono de devolución de llamada para un usuario especificado.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo función RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679551"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="9024b-104">RasAdminUserGetInfo función)</span><span class="sxs-lookup"><span data-stu-id="9024b-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="9024b-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="9024b-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="9024b-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9024b-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="9024b-107">Las aplicaciones deben usar la función [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="9024b-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="9024b-108">La función **RasAdminUserGetInfo** obtiene la información de los permisos ras y del número de teléfono de devolución de llamada para un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="9024b-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9024b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9024b-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="9024b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9024b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9024b-111">*lpszUserAccountServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9024b-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9024b-112">Puntero a una cadena Unicode terminada en null que especifica el nombre del controlador de dominio principal o de reserva que tiene la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="9024b-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="9024b-113">Use la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener este nombre de servidor.</span><span class="sxs-lookup"><span data-stu-id="9024b-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="9024b-114">*lpszUser* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9024b-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9024b-115">Puntero a una cadena Unicode terminada en null que especifica el nombre del usuario para el que se va a obtener información de RAS.</span><span class="sxs-lookup"><span data-stu-id="9024b-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="9024b-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="9024b-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="9024b-117">Puntero a la estructura de [**usuario de Ras \_ \_ 0**](ras-user-0-str.md) que recibe los datos de ras para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="9024b-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9024b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9024b-118">Return value</span></span>

<span data-ttu-id="9024b-119">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9024b-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9024b-120">Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="9024b-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="9024b-121">Value</span><span class="sxs-lookup"><span data-stu-id="9024b-121">Value</span></span>                                                                                            | <span data-ttu-id="9024b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="9024b-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="9024b-123"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="9024b-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="9024b-124">Memoria insuficiente para realizar esta función.</span><span class="sxs-lookup"><span data-stu-id="9024b-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="9024b-125">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9024b-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="9024b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9024b-126">Requirements</span></span>



| <span data-ttu-id="9024b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9024b-127">Requirement</span></span> | <span data-ttu-id="9024b-128">Value</span><span class="sxs-lookup"><span data-stu-id="9024b-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9024b-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9024b-129">End of client support</span></span><br/> | <span data-ttu-id="9024b-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9024b-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9024b-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9024b-131">End of server support</span></span><br/> | <span data-ttu-id="9024b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9024b-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9024b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9024b-133">Header</span></span><br/>                | <dl> <span data-ttu-id="9024b-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9024b-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9024b-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9024b-135">Library</span></span><br/>               | <dl> <span data-ttu-id="9024b-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9024b-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9024b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9024b-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9024b-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9024b-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9024b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="9024b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9024b-140">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="9024b-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9024b-141">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="9024b-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="9024b-142">**Usuario de RAS \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="9024b-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="9024b-143">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="9024b-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="9024b-144">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9024b-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

