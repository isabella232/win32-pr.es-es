---
description: Devuelve una matriz de proveedores de protocolos Capa de sockets seguros (SSL) instalados.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Función SslEnumProtocolProviders (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073621"
---
# <a name="sslenumprotocolproviders-function"></a>Función SslEnumProtocolProviders

La **función SslEnumProtocolProviders** devuelve una matriz de proveedores de [*protocolos Capa de sockets seguros (SSL)*](/windows/desktop/SecGloss/s-gly) instalados.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwProviderCount* \[ out\]
</dt> <dd>

Puntero a un valor **DWORD** para recibir el número de proveedores de protocolo devueltos.

</dd> <dt>

*ppProviderList* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la matriz de [**estructuras NCryptProviderName.**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, los siguientes.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | El *parámetro dwFlags* no es cero.<br/>                              |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/>     |
| <dl> <dt>**NTE \_ PARÁMETRO \_ NO VÁLIDO**</dt> <dt>0x80090027L</dt> </dl> | El *parámetro pdwProviderCount* o *ppProviderList* es **NULL.**<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando haya terminado de usar la matriz de estructuras [**NCryptProviderName,**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) llame a la [**función SslFreeBuffer**](sslfreebuffer.md) para liberar la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

