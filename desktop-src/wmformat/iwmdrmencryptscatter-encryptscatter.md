---
title: Método IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: El método EncryptScatter descodifica y cifra los datos.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Método EncryptScatter formato de Windows Media
- Método EncryptScatter formato de Windows Media, interfaz IWMDRMEncryptScatter
- Interfaz IWMDRMEncryptScatter formato de Windows Media, método EncryptScatter
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
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660151"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>IWMDRMEncryptScatter:: EncryptScatter (método)

El método **EncryptScatter** descodifica y cifra los datos.

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

*cBlocks* \[ de\]
</dt> <dd>

Número de elementos de la matriz *rgBlocks* .

</dd> <dt>

*rgBlocks* \[ de\]
</dt> <dd>

Matriz de una o varias estructuras de [**\_ bloques de \_ dispersión \_ de cifrado WMDRM**](wmdrm-encrypt-scatter-block.md) . Cada elemento describe un bloque de datos que se va a descodificar y cifrar.

</dd> <dt>

*pWMCryptoData* \[ de\]
</dt> <dd>

Puntero a una estructura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contiene los parámetros de cifrado. Establezca en **null** para usar los parámetros predeterminados.

</dd> <dt>

*cbOutput* \[ de\]
</dt> <dd>

Tamaño del búfer de datos de salida pasado como *pbOutput*.

</dd> <dt>

*pbOutput* \[ enuncia\]
</dt> <dd>

Búfer de salida.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Interfaz IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





