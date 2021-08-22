---
title: Estructura WMDRMCryptoData (Wmdrmsdk.h)
description: La estructura WMDRMCryptoData contiene información sobre el algoritmo criptográfico utilizado para cifrar y descifrar el contenido.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Estructura WMDRMCryptoData windows Media Format
- Estructura de windows Formato multimedia
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
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083809"
---
# <a name="wmdrmcryptodata-structure"></a>Estructura WMDRMCryptoData

La **estructura WMDRMCryptoData** contiene información sobre el algoritmo criptográfico utilizado para cifrar y descifrar el contenido.

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

Miembro de la [**enumeración \_ DRM CRYPTO \_ TYPE**](drm-crypto-type.md) que especifica el tipo de algoritmo criptográfico.

</dd> <dt>

**qwCounterID**
</dt> <dd>

Los 64 bits altos del modo de contador AES de 128 bits. Este miembro solo se usa si el **miembro cryptoType** está establecido en **CRYPTO TYPE \_ \_ MCE**.

</dd> <dt>

**qwOffset**
</dt> <dd>

Los 64 bits inferiores del modo de contador AES de 128 bits. Este miembro solo se usa si el **miembro cryptoType** está establecido en **CRYPTO TYPE \_ \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





