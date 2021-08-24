---
title: CD3DX12_PACKED_MIP_INFO estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura DE INFORMACIÓN DE MIP EMPAQUETADA de D3D12. \_ \_ \_
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- CD3DX12_PACKED_MIP_INFO estructura
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32a4b0516560ac553b3ce6acb6972def5d0e3f84a2eb84026a0635f779a2c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752165"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>Estructura DE INFORMACIÓN \_ \_ DE MIP EMPAQUETADA DE \_ CD3DX12

Estructura auxiliar para permitir la inicialización sencilla de una estructura DE INFORMACIÓN [**\_ DE \_ MIP EMPAQUETADA \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ PACKED \_ MIP \_ INFO()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una INFORMACIÓN DE MIP EMPAQUETADA \_ \_ CD3DX12. \_

</dd> <dt>

**explicit CD3DX12 \_ PACKED \_ MIP \_ INFO(const D3D12 \_ PACKED \_ MIP \_ INFO &o)**
</dt> <dd>

Crea una nueva instancia de una información DE MIP EMPAQUETADA CD3DX12, inicializada con el contenido de otra estructura DE INFORMACIÓN DE MIP EMPAQUETADA \_ \_ \_ [**\_ \_ \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)

</dd> <dt>

**CD3DX12 \_ PACKED \_ MIP \_ INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**
</dt> <dd>

Crea una nueva instancia de una información de MIP EMPAQUETADA CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**operator const D3D12 \_ PACKED \_ MIP \_ INFO&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE \_ MIP EMPAQUETADA DE D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





