---
title: Método Encrypt de IWMSecureBuffer (wmdrmsdk. h)
description: El método Encrypt cifra un puntero de datos.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Método de cifrado de Windows Media Format
- Método Encrypt formato de Windows Media, interfaz IWMSecureBuffer
- Interfaz IWMSecureBuffer formato de Windows Media, método Encrypt
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
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709249"
---
# <a name="iwmsecurebufferencrypt-method"></a>IWMSecureBuffer:: Encrypt (método)

El método **Encrypt** cifra un puntero de datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSecureChannel* \[ de\]
</dt> <dd>

Puntero a una interfaz de canal seguro que contiene el puntero de datos que se va a cifrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Utilice este método para cifrar los punteros de datos de manera que se puedan enviar a través de límites de DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descifrado**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Interfaz IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





