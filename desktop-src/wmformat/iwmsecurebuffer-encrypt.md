---
title: Método IWMSecureBuffer Encrypt (Wmdrmsdk.h)
description: El método Encrypt cifra un puntero de datos.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Cifrado del método windows Media Format
- Cifrado del método windows Media Format , interfaz IWMSecureBuffer
- IWMSecureBuffer interface windows Media Format , Encrypt method
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e5badce8249e5d6b9d2460fec0e72ef4ca4b81f5b8ffa0d3edd83729f98bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808315"
---
# <a name="iwmsecurebufferencrypt-method"></a>IWMSecureBuffer::Encrypt (método)

El **método Encrypt** cifra un puntero de datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSecureChannel* \[ En\]
</dt> <dd>

Puntero a una interfaz de canal seguro que contiene el puntero de datos que se cifrará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Use este método para cifrar punteros de datos para que se puedan enviar a través de los límites de DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descifrar**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**IWMSecureBuffer (interfaz)**](iwmsecurebuffer.md)
</dt> </dl>

 

 





