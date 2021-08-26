---
title: Función TLSLicenseEnumNext
description: Continúa desde una llamada anterior a la función TLSLicenseEnumBegin y devuelve la siguiente licencia instalada en un servidor de licencias de Escritorio remoto que coincida con los criterios de búsqueda.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Función TLSLicenseEnumNext Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945c0afb931770a36049342f32c71613bd8fb1a0a9b16142c1ffbc6a67ccc288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986805"
---
# <a name="tlslicenseenumnext-function"></a>Función TLSLicenseEnumNext

Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y devuelve la siguiente licencia instalada en un servidor de licencias de Escritorio remoto que coincida con los criterios de búsqueda.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ En\]
</dt> <dd>

Identificador de un Escritorio remoto de licencias. Especifique un identificador abierto por la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*lpLicense* \[ En\]
</dt> <dd>

Puntero a una [**estructura LSLicense**](lslicense.md) que recibe la siguiente licencia que coincide con los criterios de búsqueda.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

La llamada se realiza correctamente.

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ NO \_ TENGO \_ MÁS \_ DATOS** (4001)


</dt> <dd>

No hay más licencias que coincidan con los criterios de búsqueda.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ ERROR \_ INTERNO** (5001)


</dt> <dd>

Error interno en el servidor de licencias.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ SECUENCIA \_ NO VÁLIDA** (5006)


</dt> <dd>

La secuencia de llamada no era válida. Debe llamar a [**la función TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) antes de esto.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ BUSY** (5007)


</dt> <dd>

El servidor de licencias está demasiado ocupado para procesar la solicitud.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

No se puede procesar la solicitud debido a memoria insuficiente.

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

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

