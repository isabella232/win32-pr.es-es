---
title: TLSKeyPackEnumBegin función)
description: Comienza la enumeración a través de todos los paquetes de claves instalados en un servidor de licencias de Escritorio remoto basado en criterios de búsqueda.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSKeyPackEnumBegin
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359849"
---
# <a name="tlskeypackenumbegin-function"></a>TLSKeyPackEnumBegin función)

Comienza la enumeración a través de todos los paquetes de claves instalados en un servidor de licencias de Escritorio remoto basado en criterios de búsqueda.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ de\]
</dt> <dd>

Identificador de un servidor de licencias de Escritorio remoto. Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*dwSearchParm* \[ de\]
</dt> <dd>

Especifica los criterios de búsqueda. Este parámetro se reserva para uso futuro y debe contener 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ de\]
</dt> <dd>

Especifica si se deben buscar coincidencias con todos los valores de búsqueda.

</dd> <dt>

*lpSearchParm* \[ de\]
</dt> <dd>

Puntero a una estructura [**LSKeyPack**](lskeypack.md) que especifica los parámetros de búsqueda que se van a buscar.

</dd> <dt>

*pdwErrCode* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)


</dt> <dd>

La llamada se realiza correctamente.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ \_ error interno** (5001)


</dt> <dd>

Error interno en el servidor de licencias.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ secuencia no válida** (5006)


</dt> <dd>

La secuencia de llamada no era válida. Lo más probable es que una enumeración anterior no haya finalizado.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ servidor \_ ocupado** (5007)


</dt> <dd>

El servidor de licencias está demasiado ocupado para procesar la solicitud.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

No se puede procesar la solicitud porque no hay memoria suficiente.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ datos no válidos** (5009)


</dt> <dd>

Los datos del parámetro de búsqueda no son válidos.

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

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

