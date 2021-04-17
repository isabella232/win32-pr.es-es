---
description: Contiene un vector de inicialización (IV) para el cifrado de cifrado del modo Estándar de cifrado avanzado CTR (AES-CTR) de 128 bits.
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: D3DAES_CTR_IV estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360107"
---
# <a name="d3daes_ctr_iv-structure"></a>\_Estructura D3DAES CTR \_ IV

Contiene un vector de inicialización (IV) para el cifrado de cifrado del modo Estándar de cifrado avanzado CTR (AES-CTR) de 128 bits.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a>Miembros

<dl> <dt>

**IV**
</dt> <dd>

El IV, en formato Big-Endian.

</dd> <dt>

**Recuento**
</dt> <dd>

Recuento de bloques, en formato Big-Endian.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura **D3DAES \_ CTR \_ IV** y la estructura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) son equivalentes.

Para obtener más información, consulte [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h (incluye d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




