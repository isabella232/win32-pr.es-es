---
description: Abre un identificador para una clave privada.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Función SslOpenPrivateKey (Sslprovider.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250346"
---
# <a name="sslopenprivatekey-function"></a>Función SslOpenPrivateKey

La **función SslOpenPrivateKey** abre un identificador para una [*clave privada.*](/windows/desktop/SecGloss/p-gly)

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

*hSslProvider* \[ En\]
</dt> <dd>

Identificador de la instancia [*del proveedor Capa de sockets seguros protocolo*](/windows/desktop/SecGloss/s-gly) ssl (ssl).

</dd> <dt>

*phPrivateKey* \[ out\]
</dt> <dd>

Dirección de un búfer en el que se va a escribir el identificador en la clave privada.

Cuando haya terminado de usar la clave, debe liberar *phPrivateKey* llamando a la [**función SslFreeObject.**](sslfreeobject.md)

</dd> <dt>

*pCertContext* \[ En\]
</dt> <dd>

Dirección del certificado del que se va a obtener la clave privada.

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
| <dl> <dt>**NTE \_ IDENTIFICADOR \_ NO VÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | El *identificador hSslProvider* no es válido.<br/>                       |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro phPrivateKey* *o pCertContext* es **NULL.**<br/>   |



 

## <a name="remarks"></a>Observaciones

La clave privada obtenida forma parte de un [*par de claves*](/windows/desktop/SecGloss/p-gly) pública y privada dentro de un [*certificado*](/windows/desktop/SecGloss/c-gly). Esta función simplemente extrae la clave privada del certificado especificado por el *parámetro pCertContext.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

