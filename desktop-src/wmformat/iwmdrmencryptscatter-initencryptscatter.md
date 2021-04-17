---
title: Método IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: El método InitEncryptScatter inicializa la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Método InitEncryptScatter formato de Windows Media
- Método InitEncryptScatter formato de Windows Media, interfaz IWMDRMEncryptScatter
- Interfaz IWMDRMEncryptScatter formato de Windows Media, método InitEncryptScatter
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660652"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>IWMDRMEncryptScatter:: InitEncryptScatter (método)

El método **InitEncryptScatter** inicializa la interfaz **IWMDRMEncryptScatter** para su uso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cStreams* \[ de\]
</dt> <dd>

Número de elementos de la matriz *rgInfos* . Este es también el número de flujos que se incluyen en los datos que se van a cifrar.

</dd> <dt>

*rgInfos* \[ de\]
</dt> <dd>

Matriz de una o varias estructuras de [**\_ \_ \_ información de dispersión cifrada de WMDRM**](wmdrm-encrypt-scatter-info.md) . Cada elemento contiene información de cifrado de una secuencia. El número de elementos de esta matriz debe ser igual al valor de *cStreams*.

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
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





