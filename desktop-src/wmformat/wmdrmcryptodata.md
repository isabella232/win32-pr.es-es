---
title: Estructura WMDRMCryptoData (wmdrmsdk. h)
description: La estructura WMDRMCryptoData contiene información sobre el algoritmo criptográfico que se usa para cifrar y descifrar contenido.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Estructura WMDRMCryptoData formato de Windows Media
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699979"
---
# <a name="wmdrmcryptodata-structure"></a>Estructura WMDRMCryptoData

La estructura **WMDRMCryptoData** contiene información sobre el algoritmo criptográfico que se usa para cifrar y descifrar contenido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cryptoType**
</dt> <dd>

Miembro de la enumeración de [**\_ \_ tipo criptográfico de DRM**](drm-crypto-type.md) que especifica el tipo de algoritmo criptográfico.

</dd> <dt>

**qwCounterID**
</dt> <dd>

Los bits 64 altos del modo de contador AES de 128 bits. Este miembro solo se utiliza si el miembro **cryptoType** está establecido en el **tipo de cifrado \_ \_ MCE**.

</dd> <dt>

**qwOffset**
</dt> <dd>

Los bits 64 bajos del modo de contador AES de 128 bits. Este miembro solo se utiliza si el miembro **cryptoType** está establecido en el **tipo de cifrado \_ \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





