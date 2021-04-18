---
title: Función RasAdminServerGetInfo (rassapi. h)
description: La función RasAdminServerGetInfo obtiene la configuración de servidor de un servidor RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo función RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680702"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="6f9fa-104">RasAdminServerGetInfo función)</span><span class="sxs-lookup"><span data-stu-id="6f9fa-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="6f9fa-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="6f9fa-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="6f9fa-107">Las aplicaciones deben usar la función [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="6f9fa-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="6f9fa-108">La función **RasAdminServerGetInfo** obtiene la configuración de servidor de un servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9fa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f9fa-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="6f9fa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f9fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9fa-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f9fa-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9fa-112">Puntero a una cadena Unicode terminada en **null** que especifica el nombre del servidor RAS de Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="6f9fa-113">Si este parámetro es **null**, la función devuelve información sobre el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="6f9fa-114">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="6f9fa-115">*pRasServer0* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f9fa-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9fa-116">Puntero a la estructura del [**servidor de Ras \_ \_ 0**](ras-server-0-str.md) que recibe el número de puertos configurados en el servidor, el número de puertos actualmente en uso y el número de versión del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9fa-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f9fa-117">Return value</span></span>

<span data-ttu-id="6f9fa-118">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="6f9fa-119">Si se produce un error en la función, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="6f9fa-120">Los códigos de error posibles incluyen los devueltos por [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para la función [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="6f9fa-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="6f9fa-121">No hay información de error extendida para esta función; no llame a **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="6f9fa-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9fa-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f9fa-122">Remarks</span></span>

<span data-ttu-id="6f9fa-123">Para enumerar todos los servidores RAS de un dominio, llame a la función [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) y especifique el \_ tipo VP \_ para el parámetro *ServerType* .</span><span class="sxs-lookup"><span data-stu-id="6f9fa-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9fa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f9fa-124">Requirements</span></span>



| <span data-ttu-id="6f9fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9fa-125">Requirement</span></span> | <span data-ttu-id="6f9fa-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f9fa-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9fa-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6f9fa-127">End of client support</span></span><br/> | <span data-ttu-id="6f9fa-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f9fa-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="6f9fa-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6f9fa-129">End of server support</span></span><br/> | <span data-ttu-id="6f9fa-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f9fa-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="6f9fa-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f9fa-131">Header</span></span><br/>                | <dl> <span data-ttu-id="6f9fa-132"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f9fa-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f9fa-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f9fa-133">Library</span></span><br/>               | <dl> <span data-ttu-id="6f9fa-134"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f9fa-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f9fa-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f9fa-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6f9fa-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f9fa-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9fa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f9fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9fa-138">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="6f9fa-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="6f9fa-139">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="6f9fa-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="6f9fa-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="6f9fa-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="6f9fa-141">**\_Servidor RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6f9fa-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

