---
description: Devuelve una matriz de proveedores de protocolo de protocolo Capa de sockets seguros (SSL) instalados.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Función SslEnumProtocolProviders (Sslprovider. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279311"
---
# <a name="sslenumprotocolproviders-function"></a>SslEnumProtocolProviders función)

La función **SslEnumProtocolProviders** devuelve una matriz de proveedores de protocolos de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) instalados.

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

*pdwProviderCount* \[ enuncia\]
</dt> <dd>

Un puntero a un valor **DWORD** para recibir el número de proveedores de protocolo devueltos.

</dd> <dt>

*ppProviderList* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe la matriz de estructuras [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

Si se produce un error en la función, devuelve un valor de error distinto de cero.

Los códigos de retorno posibles incluyen, entre otros, lo siguiente.



| Código o valor devuelto                                                                                                                                                       | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt> </dl>         | El parámetro *dwFlags* no es cero.<br/>                              |
| <dl> <dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt> </dl>         | No hay suficiente memoria disponible para asignar los búferes necesarios.<br/>     |
| <dl> <dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt> </dl> | El parámetro *pdwProviderCount* o *ppProviderList* es **null**.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando haya terminado de usar la matriz de estructuras [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , llame a la función [**SslFreeBuffer**](sslfreebuffer.md) para liberar la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

