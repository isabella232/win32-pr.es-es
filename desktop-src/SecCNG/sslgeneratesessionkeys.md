---
description: Genera un conjunto de claves de sesión de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Función SslGenerateSessionKeys (Sslprovider. h)
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
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669988"
---
# <a name="sslgeneratesessionkeys-function"></a>SslGenerateSessionKeys función)

La función **SslGenerateSessionKeys** genera un conjunto de claves de sesión de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

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

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor del protocolo SSL.

</dd> <dt>

*hMasterKey* \[ de\]
</dt> <dd>

Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*phReadKey* \[ enuncia\]
</dt> <dd>

Puntero al identificador de clave de lectura devuelto.

</dd> <dt>

*phWriteKey* \[ enuncia\]
</dt> <dd>

Puntero al identificador de clave de escritura devuelto.

</dd> <dt>

*pParameterList* \[ de\]
</dt> <dd>

Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves. El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza. Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/> |
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | Uno de los identificadores proporcionados no es válido.<br/>                     |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phReadKey* o *phWriteKey* es NULL.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

