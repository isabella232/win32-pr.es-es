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
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360944"
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



 

## <a name="remarks"></a>Observaciones

Use este método para cifrar punteros de datos para que se puedan enviar a través de los límites de DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Descifrar**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**IWMSecureBuffer (interfaz)**](iwmsecurebuffer.md)
</dt> </dl>

 

 





