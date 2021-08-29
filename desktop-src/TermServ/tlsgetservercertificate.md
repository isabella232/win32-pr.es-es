---
title: Función TLSGetServerCertificate
description: Devuelve el certificado del servidor Escritorio remoto licencias.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Función TLSGetServerCertificate Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f32b939eff90a5043b1fc29d90534d2d51215522f1f5ff07ba45e817014936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986945"
---
# <a name="tlsgetservercertificate-function"></a>Función TLSGetServerCertificate

Devuelve el certificado del servidor Escritorio remoto licencias.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ En\]
</dt> <dd>

Identificador de un Escritorio remoto de licencias que se abre mediante una llamada a la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*bSignCert* \[ En\]
</dt> <dd>

**TRUE si** certificado de firma, **FALSE** si certificado de intercambio.

</dd> <dt>

*ppbCertBlob* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un puntero a un búfer que contiene el certificado.

</dd> <dt>

*lpdwCertBlobLen* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del certificado que se devuelve.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el código de error.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

La llamada se realiza correctamente.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ W \_ SELFSIGN \_ CERTIFICATE** (4007)


</dt> <dd>

El certificado devuelto es un certificado autofirmado.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ TEMP \_ SELFSIGN \_ CERT** (4009)


</dt> <dd>

El certificado devuelto es temporal.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ ACCESO \_ \_ DENEGADO** (5003)


</dt> <dd>

Acceso denegado:

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E \_ ALLOCATE \_ HANDLE** (5007)


</dt> <dd>

El servidor está demasiado ocupado para procesar la solicitud.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ NO \_ CERTIFICATE** (5022)


</dt> <dd>

No se puede recuperar un certificado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve los siguientes valores devueltos posibles.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

La llamada se ha realiza correctamente. Compruebe el valor del *parámetro pdwErrCode* para obtener el código de retorno de la llamada.

</dd> <dt>

**ARGUMENTO \_ RPC S NO \_ \_ VÁLIDO**
</dt> <dd>

El argumento no era válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

