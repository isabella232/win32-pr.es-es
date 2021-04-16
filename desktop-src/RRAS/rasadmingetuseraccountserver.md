---
title: Función RasAdminGetUserAccountServer (rassapi. h)
description: La función RasAdminGetUserAccountServer recupera el nombre del servidor que tiene la base de datos de cuentas de usuario. Use el nombre de servidor devuelto en las funciones RasAdminUserGetInfo y RasAdminUserSetInfo para obtener o establecer información sobre un usuario especificado.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer función RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679552"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="23362-105">RasAdminGetUserAccountServer función)</span><span class="sxs-lookup"><span data-stu-id="23362-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="23362-106">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="23362-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="23362-107">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="23362-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="23362-108">Las aplicaciones deben usar la función [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]</span><span class="sxs-lookup"><span data-stu-id="23362-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="23362-109">La función **RasAdminGetUserAccountServer** recupera el nombre del servidor que tiene la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="23362-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="23362-110">Use el nombre de servidor devuelto en las funciones [**RasAdminUserGetInfo**](rasadminusergetinfo.md) y [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obtener o establecer información sobre un usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="23362-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="23362-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23362-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="23362-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23362-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23362-113">*lpszDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23362-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23362-114">Puntero a una cadena Unicode terminada en **null** que especifica el nombre del dominio al que pertenece el servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="23362-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="23362-115">Este parámetro es **null** para las aplicaciones de administración de ras que se ejecutan en estaciones de trabajo o servidores que no son miembros de un dominio.</span><span class="sxs-lookup"><span data-stu-id="23362-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="23362-116">Si este parámetro es **null**, el parámetro *lpszServer* no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="23362-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23362-117">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="23362-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23362-118">Puntero a una cadena Unicode terminada en **null** que especifica el nombre del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="23362-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="23362-119">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="23362-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="23362-120">Este parámetro puede ser **null** si el parámetro *LpszDomain* no es **null**.</span><span class="sxs-lookup"><span data-stu-id="23362-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23362-121">*lpszUserAccountServer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23362-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23362-122">Puntero a un búfer que recibe una cadena Unicode terminada en **null** que especifica el nombre de un controlador de dominio que tiene la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="23362-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="23362-123">El búfer debe ser lo suficientemente grande como para contener el nombre del servidor (más o más).</span><span class="sxs-lookup"><span data-stu-id="23362-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="23362-124">La función antepone el nombre del servidor devuelto con los " \\ \\ " caracteres iniciales, con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="23362-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23362-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23362-125">Return value</span></span>

<span data-ttu-id="23362-126">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="23362-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="23362-127">Si se produce un error en la función, el valor devuelto puede ser el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="23362-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="23362-128">Value</span><span class="sxs-lookup"><span data-stu-id="23362-128">Value</span></span>                                                                                                    | <span data-ttu-id="23362-129">Significado</span><span class="sxs-lookup"><span data-stu-id="23362-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="23362-130"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="23362-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="23362-131">Tanto *lpszDomain* como *lpszServer* son **null**.</span><span class="sxs-lookup"><span data-stu-id="23362-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="23362-132">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="23362-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="23362-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23362-133">Remarks</span></span>

<span data-ttu-id="23362-134">La función **RasAdminGetUserAccountServer** obtiene el nombre del servidor con la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="23362-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="23362-135">Esta función requiere el nombre del servidor RAS o el nombre del dominio en el que reside el servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="23362-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="23362-136">El parámetro *lpszDomain* debe especificar un nombre de dominio válido.</span><span class="sxs-lookup"><span data-stu-id="23362-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="23362-137">Este parámetro es **null** para las aplicaciones de administración de ras que se ejecutan en servidores que no son miembros de un dominio (por ejemplo, el servidor está en su propio grupo de trabajo).</span><span class="sxs-lookup"><span data-stu-id="23362-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="23362-138">En este caso, el parámetro *lpszServer* debe especificar el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="23362-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="23362-139">Para obtener el nombre del servidor, llame a la función [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) .</span><span class="sxs-lookup"><span data-stu-id="23362-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="23362-140">Asegúrese de anteponer los caracteres "" al nombre del servidor \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="23362-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="23362-141">Si el nombre del servidor especificado por *lpszServer* es un servidor independiente (es decir, el servidor o la estación de trabajo no es miembro de un dominio), se devuelve el nombre del servidor en el búfer *lpszUserAccountServer* .</span><span class="sxs-lookup"><span data-stu-id="23362-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="23362-142">A continuación, utilice el nombre del servidor de cuentas de usuario en una llamada a la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar los usuarios en la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="23362-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="23362-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23362-143">Requirements</span></span>



| <span data-ttu-id="23362-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="23362-144">Requirement</span></span> | <span data-ttu-id="23362-145">Value</span><span class="sxs-lookup"><span data-stu-id="23362-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23362-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="23362-146">End of client support</span></span><br/> | <span data-ttu-id="23362-147">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23362-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="23362-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="23362-148">End of server support</span></span><br/> | <span data-ttu-id="23362-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23362-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="23362-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23362-150">Header</span></span><br/>                | <dl> <span data-ttu-id="23362-151"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="23362-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="23362-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23362-152">Library</span></span><br/>               | <dl> <span data-ttu-id="23362-153"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23362-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="23362-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23362-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="23362-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23362-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23362-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="23362-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23362-157">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="23362-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="23362-158">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="23362-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="23362-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="23362-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="23362-160">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="23362-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="23362-161">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="23362-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

