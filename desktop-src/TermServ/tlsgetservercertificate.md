---
title: TLSGetServerCertificate función)
description: Devuelve el certificado del servidor de licencias de Escritorio remoto.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSGetServerCertificate
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
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676663"
---
# <a name="tlsgetservercertificate-function"></a>TLSGetServerCertificate función)

Devuelve el certificado del servidor de licencias de Escritorio remoto.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

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

*hHandle* \[ de\]
</dt> <dd>

Identificador de un servidor de licencias de Escritorio remoto abierto por una llamada a la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*bSignCert* \[ de\]
</dt> <dd>

**True** si el certificado de firma es **false** si se trata de un certificado de Exchange.

</dd> <dt>

*ppbCertBlob* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un puntero a un búfer que contiene el certificado.

</dd> <dt>

*lpdwCertBlobLen* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del certificado que se devuelve.

</dd> <dt>

*pdwErrCode* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el código de error.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)


</dt> <dd>

La llamada se realiza correctamente.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificado W SELFSIGN** (4007)


</dt> <dd>

El certificado devuelto es un certificado autofirmado.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ temp \_ SELFSIGN \_ CERT** (4009)


</dt> <dd>

El certificado devuelto es temporal.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ acceso \_ denegado** (5003)


</dt> <dd>

Acceso denegado.

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E \_ \_ identificador de asignación** (5007)


</dt> <dd>

El servidor está demasiado ocupado para procesar la solicitud.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ sin \_ certificado** (5022)


</dt> <dd>

No se puede recuperar un certificado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve los siguientes posibles valores devueltos.

<dl> <dt>

**RPC \_ S \_ correcto**
</dt> <dd>

La llamada se realizó correctamente. Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.

</dd> <dt>

**\_ \_ argumento no válido de RPC S \_**
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

 

