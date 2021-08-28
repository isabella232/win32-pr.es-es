---
title: Método IWMDRMEncryptScatter EncryptScatter (Wmdrmsdk.h)
description: El método EncryptScatter desenreda y cifra los datos.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Formato multimedia de Windows del método EncryptScatter
- Método EncryptScatter windows Media Format , interfaz IWMDRMEncryptScatter
- IWMDRMEncryptScatter interface windows Media Format , EncryptScatter method
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fae3f8a40bc5468898424dcf33bf947235a632db44f4dada7f2c96b2a3a064b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839716"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Método IWMDRMEncryptScatter::EncryptScatter

El **método EncryptScatter** desanude y cifra los datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cBlocks* \[ En\]
</dt> <dd>

Número de elementos de la *matriz rgBlocks.*

</dd> <dt>

*rgBlocks* \[ En\]
</dt> <dd>

Matriz de una o varias [**estructuras DE BLOQUE DE DISPERSIÓN DE WMDRM \_ \_ ENCRYPT. \_**](wmdrm-encrypt-scatter-block.md) Cada elemento describe un bloque de datos que se va a deshacer y cifrar.

</dd> <dt>

*pWMCryptoData* \[ En\]
</dt> <dd>

Puntero a una [**estructura WMDRMCryptoData**](wmdrmcryptodata.md) que contiene parámetros de cifrado. Establezca en **NULL** para usar los parámetros predeterminados.

</dd> <dt>

*cbOutput* \[ En\]
</dt> <dd>

Tamaño del búfer de datos de salida pasado *como pbOutput*.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Búfer de salida.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





