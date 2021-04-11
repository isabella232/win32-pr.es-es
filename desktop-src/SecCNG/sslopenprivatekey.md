---
description: Abre un identificador para una clave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Función SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154089"
---
# <a name="sslopenprivatekey-function"></a>SslOpenPrivateKey función)

La función **SslOpenPrivateKey** abre un identificador para una [*clave privada*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phPrivateKey* \[ enuncia\]
</dt> <dd>

Dirección de un búfer en el que se va a escribir el identificador de la clave privada.

Cuando haya terminado de usar la clave, debe liberar *phPrivateKey* llamando a la función [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pCertContext* \[ de\]
</dt> <dd>

Dirección del certificado del que se va a obtener la clave privada.

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
| <dl> <dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt> </dl>    | El identificador de *hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *phPrivateKey* o *pCertContext* es **null**.<br/>   |



 

## <a name="remarks"></a>Observaciones

La clave privada obtenida forma parte de un [*par de claves pública y privada*](/windows/desktop/SecGloss/p-gly) dentro de un [*certificado*](/windows/desktop/SecGloss/c-gly). Esta función simplemente extrae la clave privada del certificado especificado por el parámetro *pCertContext* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

