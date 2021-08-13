---
description: Calcula el bloque de claves utilizado por el Protocolo de autenticación extensible (EAP).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Función SslComputeEapKeyBlock (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 48f657f565c239f797fd67b108ce3b18b692dfabc0248e1005465e9123ac492d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907185"
---
# <a name="sslcomputeeapkeyblock-function"></a>Función SslComputeEapKeyBlock

La **función SslComputeEapKeyBlock** calcula el bloque de claves usado por el Protocolo de autenticación extensible (EAP).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

El identificador de la instancia [*del proveedor Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) protocolo de seguridad (SSL).

</dd> <dt>

*hMasterKey* \[ En\]
</dt> <dd>

Identificador del objeto [*de clave*](/windows/desktop/SecGloss/m-gly) maestra.

</dd> <dt>

*pbRandoms* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene una concatenación de los valores aleatorios de cliente y \_ \_ aleatorios del servidor de la sesión SSL.

</dd> <dt>

*cbRandoms* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbRandoms.*

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

Dirección de un búfer que recibe la clave BLOB. El *parámetro cbOutput* contiene el tamaño de este búfer. Si este parámetro es **NULL,** esta función colocará el tamaño necesario, en bytes, en el **DWORD** al que apunta el *parámetro byteResult.*

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Longitud, en bytes, del *búfer pbOutput.*

</dd> <dt>

*pwResult* \[ out\]
</dt> <dd>

Puntero a un **valor DWORD** que especifica la longitud, en bytes, del hash escrito en el *búfer pbOutput.*

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Establezca en **NCRYPT \_ SSL SERVER \_ \_ FLAG** para indicar que se trata de una llamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.



| Código o valor devuelto                                                                                                                                                    | Descripción                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno de los identificadores proporcionados no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

