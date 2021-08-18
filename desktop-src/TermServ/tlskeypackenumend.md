---
title: Función TLSKeyPackEnumEnd
description: Continúa desde una llamada anterior a la función TLSKeyPackEnumBegin y finaliza la enumeración .
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- Función TLSKeyPackEnumEnd Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176c5d6b03fabe2e085b2582043233cd5fdc2681ef04ef07723ba5435a465863
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986925"
---
# <a name="tlskeypackenumend-function"></a>Función TLSKeyPackEnumEnd

Continúa desde una llamada anterior a la [**función TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y finaliza la enumeración .

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hHandle* \[ En\]
</dt> <dd>

Identificador de un Escritorio remoto de licencias. Especifique un identificador abierto por la [**función TLSConnectToLsServer.**](tlsconnecttolsserver.md)

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

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ IDENTIFICADOR \_ NO VÁLIDO** (5005)


</dt> <dd>

El identificador no es válido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve los siguientes valores devueltos posibles.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

La llamada se ha realiza correctamente. Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.

</dd> <dt>

**RPC \_ S \_ INVALID \_ ARG**
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

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> </dl>

 

