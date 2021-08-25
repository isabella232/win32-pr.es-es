---
description: La enumeración CAPICOM \_ KEY STORAGE FLAG define las marcas de almacenamiento de \_ \_ claves.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: CAPICOM_KEY_STORAGE_FLAG enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cb1c2c4761403223c8ed0eb225709fbd189127bc9d56d60b82a534e2bc15b8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879095"
---
# <a name="capicom_key_storage_flag-enumeration"></a>CAPICOM \_ KEY STORAGE FLAG \_ \_ (enumeración)

La **enumeración CAPICOM \_ KEY STORAGE \_ \_ FLAG** define las marcas de almacenamiento de claves.

## <a name="members"></a>Miembros



| Miembro                                     | Descripción                           | Value |
|--------------------------------------------|---------------------------------------|-------|
| **CAPICOM \_ KEY \_ STORAGE \_ DEFAULT**         | Almacenamiento de claves predeterminado.<br/>       | 0     |
| **ALMACENAMIENTO DE CLAVES \_ CAPICOM \_ \_ EXPORTABLE**      | La clave se puede exportar.<br/>     | 1     |
| **CAPICOM \_ KEY \_ STORAGE \_ USER \_ PROTECTED** | La clave está protegida por el usuario.<br/> | 2     |



## <a name="remarks"></a>Comentarios

El método siguiente usa esta enumeración:

-   [**Certificate.Load**](certificate-load.md)
-   [**Store.Load**](store-load.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




