---
title: Función InternetGetProxyInfo
description: Recupera los datos de proxy para tener acceso a los recursos especificados.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Función InternetGetProxyInfo WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422328"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="4b2c3-104">Función InternetGetProxyInfo</span><span class="sxs-lookup"><span data-stu-id="4b2c3-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="4b2c3-105">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-105">This function is deprecated.</span></span> <span data-ttu-id="4b2c3-106">En el caso de la compatibilidad con AutoProxy, use HTTP Services (WinHTTP) versión 5,1 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="4b2c3-107">Para obtener más información, consulte [compatibilidad con el AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="4b2c3-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="4b2c3-108">Recupera los datos de proxy para tener acceso a los recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="4b2c3-109">Solo se puede llamar a esta función mediante una vinculación dinámica a "JSProxy.dll".</span><span class="sxs-lookup"><span data-stu-id="4b2c3-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2c3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b2c3-110">Syntax</span></span>

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a><span data-ttu-id="4b2c3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b2c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b2c3-112">*lpszUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-113">Puntero a una cadena terminada en null que especifica la dirección URL del recurso HTTP de destino.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="4b2c3-114">*dwUrlLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-115">Tamaño, en bytes, de la dirección URL a la que apunta *lpszUrl*.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="4b2c3-116">*lpszUrlHostName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-117">Puntero a una cadena terminada en null que especifica el nombre de host de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="4b2c3-118">*dwUrlHostNameLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-119">Tamaño, en bytes, del nombre de host al que apunta *lpszUrlHostName*.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="4b2c3-120">*lplpszProxyHostName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-121">Puntero a la dirección de un búfer que recibe la dirección URL del proxy que se va a usar en una solicitud HTTP para el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="4b2c3-122">La aplicación es responsable de liberar esta cadena.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="4b2c3-123">*lpdwProxyHostNameLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b2c3-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2c3-124">Puntero a una variable que recibe el tamaño, en bytes, de la cadena devuelta en el búfer de *lplpszProxyHostName* .</span><span class="sxs-lookup"><span data-stu-id="4b2c3-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b2c3-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b2c3-125">Return value</span></span>

<span data-ttu-id="4b2c3-126">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="4b2c3-127">Para obtener los datos de error extendidos, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="4b2c3-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b2c3-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b2c3-128">Remarks</span></span>

<span data-ttu-id="4b2c3-129">Para llamar a **InternetGetProxyInfo**, debe vincular dinámicamente a él mediante el tipo de puntero de función definido **pfnInternetGetProxyInfo**.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="4b2c3-130">El siguiente fragmento de código muestra cómo declarar una instancia de este tipo de puntero de función y, a continuación, inicializarla y llamarla.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

<span data-ttu-id="4b2c3-131">Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain o los constructores y destructores de objetos globales.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="4b2c3-132">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="4b2c3-133">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="4b2c3-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="4b2c3-134">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="4b2c3-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b2c3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b2c3-135">Requirements</span></span>

| <span data-ttu-id="4b2c3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b2c3-136">Requirement</span></span> | <span data-ttu-id="4b2c3-137">Value</span><span class="sxs-lookup"><span data-stu-id="4b2c3-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2c3-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b2c3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4b2c3-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b2c3-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4b2c3-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b2c3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4b2c3-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b2c3-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b2c3-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b2c3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b2c3-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b2c3-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="4b2c3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b2c3-144">See also</span></span>

[<span data-ttu-id="4b2c3-145">**InternetInitializeAutoProxyDll**</span><span class="sxs-lookup"><span data-stu-id="4b2c3-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="4b2c3-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4b2c3-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="4b2c3-147">**DetectAutoProxyUrl**</span><span class="sxs-lookup"><span data-stu-id="4b2c3-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
