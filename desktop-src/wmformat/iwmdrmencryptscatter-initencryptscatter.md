---
title: Método IWMDRMEncryptScatter InitEncryptScatter (Wmdrmsdk.h)
description: El método InitEncryptScatter inicializa la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Método InitEncryptScatter windows Media Format
- Método InitEncryptScatter windows Media Format , interfaz IWMDRMEncryptScatter
- IWMDRMEncryptScatter interface windows Media Format , InitEncryptScatter method
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251463"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>IWMDRMEncryptScatter::InitEncryptScatter (método)

El **método InitEncryptScatter** inicializa la **interfaz IWMDRMEncryptScatter** para su uso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cStreams* \[ En\]
</dt> <dd>

Número de elementos de la *matriz rgInfos.* También es el número de secuencias que se incluyen en los datos que se van a cifrar.

</dd> <dt>

*rgInfos* \[ En\]
</dt> <dd>

Matriz de una o varias [**estructuras DE INFORMACIÓN DE \_ DISPERSIÓN DE CIFRADO DE \_ \_ WMDRM.**](wmdrm-encrypt-scatter-info.md) Cada elemento contiene información de cifrado para una secuencia. El número de elementos de esta matriz debe ser igual al valor de *cStreams*.

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
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter (Interfaz)**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





