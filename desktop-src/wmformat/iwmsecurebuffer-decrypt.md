---
title: Método Decrypt de IWMSecureBuffer (Wmdrmsdk.h)
description: El método Decrypt descifra un puntero de datos cifrado mediante una llamada al método Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Descifrar formato multimedia de windows del método
- Descifrar el método windows Media Format , interfaz IWMSecureBuffer
- IWMSecureBuffer interfaz windows Media Format , Decrypt (método)
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267119"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer::D ecrypt (método)

El **método Decrypt** descifra un puntero de datos cifrado mediante una llamada al método [**Encrypt.**](iwmsecurebuffer-encrypt.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSecureChannel* \[ En\]
</dt> <dd>

Puntero a una interfaz de canal seguro que contiene el puntero de datos cifrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Cifrar**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**IWMSecureBuffer (interfaz)**](iwmsecurebuffer.md)
</dt> </dl>

 

 





