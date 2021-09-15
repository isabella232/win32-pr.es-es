---
title: Función InternetGetProxyInfo
description: Recupera los datos de proxy para acceder a los recursos especificados.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Función WinINet internetGetProxyInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567244"
---
# <a name="internetgetproxyinfo-function"></a>Función InternetGetProxyInfo

> [!NOTE]
> Esta función es desusada. Para admitir el proxy automático, use la versión 5.1 de servicios HTTP (WinHTTP) en su lugar. Para más información, consulte [Compatibilidad con WinHTTP AutoProxy.](../winhttp/winhttp-autoproxy-support.md)

Recupera los datos de proxy para acceder a los recursos especificados. Solo se puede llamar a esta función si se vincula dinámicamente a "JSProxy.dll".

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

*lpszUrl* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la dirección URL del recurso HTTP de destino.

</dd> <dt>

*dwUrlLength* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la dirección URL a la que *apunta lpszUrl.*

</dd> <dt>

*lpszUrlHostName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de host de la dirección URL de destino.

</dd> <dt>

*dwUrlHostNameLength* \[ En\]
</dt> <dd>

Tamaño, en bytes, del nombre de host al que *apunta lpszUrlHostName*.

</dd> <dt>

*lplpszProxyHostName* \[ out\]
</dt> <dd>

Puntero a la dirección de un búfer que recibe la dirección URL del proxy que se usará en una solicitud HTTP para el recurso especificado. La aplicación es responsable de liberar esta cadena.

</dd> <dt>

*lpdwProxyHostNameLength* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño, en bytes, de la cadena devuelta en el búfer *lplpszProxyHostName.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario. Para obtener datos de error extendidos, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Para llamar **a InternetGetProxyInfo**, debe vincularlo dinámicamente mediante el tipo de puntero de función **definido pfnInternetGetProxyInfo**. El fragmento de código siguiente muestra cómo declarar una instancia de este tipo de puntero de función y, a continuación, inicializar y llamarla.

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

Al igual que todos los demás aspectos de la API de WinINet, no se puede llamar a esta función de forma segura desde DllMain ni desde los constructores y destructores de objetos globales.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para implementaciones de servidor o servicios, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Consulte también

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
