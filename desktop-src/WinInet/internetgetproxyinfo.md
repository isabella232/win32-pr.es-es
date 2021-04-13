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
# <a name="internetgetproxyinfo-function"></a>Función InternetGetProxyInfo

> [!NOTE]
> Esta función es desusada. En el caso de la compatibilidad con AutoProxy, use HTTP Services (WinHTTP) versión 5,1 en su lugar. Para obtener más información, consulte [compatibilidad con el AutoProxy WinHTTP](../winhttp/winhttp-autoproxy-support.md).

Recupera los datos de proxy para tener acceso a los recursos especificados. Solo se puede llamar a esta función mediante una vinculación dinámica a "JSProxy.dll".

## <a name="syntax"></a>Sintaxis

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

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszUrl* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica la dirección URL del recurso HTTP de destino.

</dd> <dt>

*dwUrlLength* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la dirección URL a la que apunta *lpszUrl*.

</dd> <dt>

*lpszUrlHostName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de host de la dirección URL de destino.

</dd> <dt>

*dwUrlHostNameLength* \[ de\]
</dt> <dd>

Tamaño, en bytes, del nombre de host al que apunta *lpszUrlHostName*.

</dd> <dt>

*lplpszProxyHostName* \[ enuncia\]
</dt> <dd>

Puntero a la dirección de un búfer que recibe la dirección URL del proxy que se va a usar en una solicitud HTTP para el recurso especificado. La aplicación es responsable de liberar esta cadena.

</dd> <dt>

*lpdwProxyHostNameLength* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de la cadena devuelta en el búfer de *lplpszProxyHostName* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario. Para obtener los datos de error extendidos, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Para llamar a **InternetGetProxyInfo**, debe vincular dinámicamente a él mediante el tipo de puntero de función definido **pfnInternetGetProxyInfo**. El siguiente fragmento de código muestra cómo declarar una instancia de este tipo de puntero de función y, a continuación, inicializarla y llamarla.

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

Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain o los constructores y destructores de objetos globales.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Vea también

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
