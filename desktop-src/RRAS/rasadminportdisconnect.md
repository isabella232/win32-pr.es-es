---
title: Función RasAdminPortDisconnect (rassapi. h)
description: La función RasAdminPortDisconnect desconecta un puerto que está actualmente en uso.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect función RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680704"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="f900a-104">RasAdminPortDisconnect función)</span><span class="sxs-lookup"><span data-stu-id="f900a-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="f900a-105">\[Esta función se proporciona solo para la compatibilidad con versiones anteriores de Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="f900a-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="f900a-106">Devuelve la \_ llamada \_ de error no \_ implementada en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f900a-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="f900a-107">Las aplicaciones deben usar la función [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]</span><span class="sxs-lookup"><span data-stu-id="f900a-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="f900a-108">La función **RasAdminPortDisconnect** desconecta un puerto que está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="f900a-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="f900a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f900a-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="f900a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f900a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f900a-111">*lpszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f900a-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f900a-112">Puntero a una cadena Unicode terminada en null que especifica el nombre del servidor RAS de Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f900a-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="f900a-113">Especifique el nombre con caracteres iniciales " \\ \\ ", con el formato: \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="f900a-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="f900a-114">*lpszPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f900a-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f900a-115">Puntero a una cadena Unicode terminada en null que especifica el nombre del puerto en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f900a-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f900a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f900a-116">Return value</span></span>

<span data-ttu-id="f900a-117">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f900a-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f900a-118">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="f900a-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="f900a-119">Value</span><span class="sxs-lookup"><span data-stu-id="f900a-119">Value</span></span>                                                                                               | <span data-ttu-id="f900a-120">Significado</span><span class="sxs-lookup"><span data-stu-id="f900a-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f900a-121"><dt>**ERROR \_ de \_ Puerto no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="f900a-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="f900a-122">El puerto especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="f900a-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="f900a-123"><dt>**NERR \_ UserNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="f900a-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="f900a-124">El puerto no está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="f900a-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="f900a-125">No hay información de error extendida para esta función; no llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="f900a-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="f900a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f900a-126">Requirements</span></span>



| <span data-ttu-id="f900a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f900a-127">Requirement</span></span> | <span data-ttu-id="f900a-128">Value</span><span class="sxs-lookup"><span data-stu-id="f900a-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f900a-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f900a-129">End of client support</span></span><br/> | <span data-ttu-id="f900a-130">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f900a-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f900a-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f900a-131">End of server support</span></span><br/> | <span data-ttu-id="f900a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f900a-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f900a-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f900a-133">Header</span></span><br/>                | <dl> <span data-ttu-id="f900a-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f900a-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="f900a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f900a-135">Library</span></span><br/>               | <dl> <span data-ttu-id="f900a-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f900a-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f900a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f900a-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f900a-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f900a-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f900a-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f900a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f900a-140">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="f900a-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="f900a-141">Funciones de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="f900a-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

