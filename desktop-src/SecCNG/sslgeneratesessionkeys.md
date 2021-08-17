---
description: Genera un conjunto de claves de sesión Capa de sockets seguros protocolo ssl (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Función SslGenerateSessionKeys (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3a9d7a25e5dd2035bd0b060ae11904e351489309b3a5e3c65c0e1582dce77500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906177"
---
# <a name="sslgeneratesessionkeys-function"></a>Función SslGenerateSessionKeys

La **función SslGenerateSessionKeys** genera un conjunto de claves [*de Capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) de sesión (SSL).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hMasterKey* \[ En\]
</dt> <dd>

Identificador del objeto [*de clave*](/windows/desktop/SecGloss/m-gly) maestra.

</dd> <dt>

*phReadKey* \[ out\]
</dt> <dd>

Puntero al identificador de clave de lectura devuelto.

</dd> <dt>

*phWriteKey* \[ out\]
</dt> <dd>

Puntero al identificador de clave de escritura devuelto.

</dd> <dt>

*pParameterList* \[ En\]
</dt> <dd>

Puntero a una matriz de búferes [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y del conjunto de cifrado que se usa. Como mínimo, la lista contendrá búferes que contienen los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phReadKey* *o phWriteKey* es NULL.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

