---
title: Método de descifrado IWMSecureBuffer (wmdrmsdk. h)
description: El método de descifrado descifra un puntero de datos que se cifró llamando al método Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Método de descifrado formato de Windows Media
- Método de descifrado formato de Windows Media, interfaz IWMSecureBuffer
- Interfaz IWMSecureBuffer formato de Windows Media, descifrar método
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671808"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer::D método ECRYPT

El método de **descifrado** descifra un puntero de datos que se cifró llamando al método [**Encrypt**](iwmsecurebuffer-encrypt.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSecureChannel* \[ de\]
</dt> <dd>

Puntero a una interfaz de canal seguro que contiene el puntero de datos cifrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cifrado**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Interfaz IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





