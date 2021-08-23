---
title: Método IWMDRMEncryptScatter InitEncryptScatter (Wmdrmsdk.h)
description: El método InitEncryptScatter inicializa la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Método InitEncryptScatter windows Media Format
- Método InitEncryptScatter windows Media Format , interfaz IWMDRMEncryptScatter
- IWMDRMEncryptScatter interface windows Media Format , Método InitEncryptScatter
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
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027763"
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

Matriz de una o varias estructuras [**DE INFORMACIÓN DE DISPERSIÓN DE WMDRM \_ \_ ENCRYPT. \_**](wmdrm-encrypt-scatter-info.md) Cada elemento contiene información de cifrado para una secuencia. El número de elementos de esta matriz debe ser igual al valor de *cStreams*.

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

[**Interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





