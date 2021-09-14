---
title: Función TLSLicenseEnumBegin
description: Comienza la enumeración de licencias emitidas por el servidor de Escritorio remoto en función de los criterios de búsqueda.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Función TLSLicenseEnumBegin Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243507"
---
# <a name="tlslicenseenumbegin-function"></a>Función TLSLicenseEnumBegin

Comienza la enumeración de licencias emitidas por el servidor de Escritorio remoto en función de los criterios de búsqueda.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ En\]
</dt> <dd>

Identificador de un Escritorio remoto de licencias. Especifique un identificador abierto por la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

</dd> <dt>

*dwSearchParm* \[ En\]
</dt> <dd>

Especifica los criterios de búsqueda. El parámetro puede ser uno o una combinación de los valores que se describen en la lista siguiente. El parámetro especifica el tipo de paquete de claves y el paquete de claves que se va a buscar.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ BUSCAR \_ LICENSEID** (0x00000001)


</dt> <dd>

Busque por identificador de licencia.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ SEARCH \_ KEYPACKID** (0x00000002)


</dt> <dd>

Busque por identificador de paquete de claves.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ SEARCH \_ MACHINENAME** (0x00000008)


</dt> <dd>

Busque por nombre de máquina.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ NOMBRE \_ DE USUARIO DE** BÚSQUEDA (0x00000010)


</dt> <dd>

Busque por nombre de usuario.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ SEARCH \_ ISSUEDATE** (0x00000080)


</dt> <dd>

Buscar por fecha de problema.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ BUSCAR \_ EXPIREDATE** (0x00000100)


</dt> <dd>

Buscar por fecha de expiración.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ BUSCAR \_ NUMLICENSES** (0x00000200)


</dt> <dd>

Buscar por número de licencias.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ ESTADO \_ DE LA ENTRADA \_ DE** BÚSQUEDA (0x20000000)


</dt> <dd>

Buscar por estado de entrada.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ EXSEARCH \_ LICENSESTATUS** (0x00100000)


</dt> <dd>

Buscar por estado de licencia.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ BUSCAR \_ TODO** (0xFFFFFFFF)


</dt> <dd>

Busque todas las licencias.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ En\]
</dt> <dd>

Especifica si se deben coincidir todos los valores de búsqueda.

</dd> <dt>

*lpSearchParm* \[ En\]
</dt> <dd>

Puntero a una [**estructura LSLicense**](lslicense.md) que especifica los parámetros de búsqueda que se buscarán.

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

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ ERROR \_ INTERNO** (5001)


</dt> <dd>

Error interno en el servidor de licencias.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ SECUENCIA \_ NO VÁLIDA** (5006)


</dt> <dd>

La secuencia de llamada no era válida. Lo más probable es que no haya finalizado una enumeración anterior.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ BUSY** (5007)


</dt> <dd>

El servidor de licencias está demasiado ocupado para procesar la solicitud.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

No se puede procesar la solicitud debido a una memoria insuficiente.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ DATOS NO \_ VÁLIDOS** (5009)


</dt> <dd>

Los datos del parámetro de búsqueda no son válidos.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve los siguientes valores devueltos posibles.

<dl> <dt>

**RPC \_ S \_ CORRECTO**
</dt> <dd>

La llamada se ha realiza correctamente. Compruebe el valor del *parámetro pdwErrCode* para obtener el código de retorno de la llamada.

</dd> <dt>

**RPC \_ S ARGUMENTO NO \_ \_ VÁLIDO**
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

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

