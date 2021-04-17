---
title: CD3DX12_PACKED_MIP_INFO estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de información de MIP empaquetada D3D12 \_ \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Estructura de CD3DX12_PACKED_MIP_INFO
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
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707771"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>CD3DX12 \_ \_ estructura de información de MIP empaquetada \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ información de MIP empaquetada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

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

**CD3DX12 \_ información de MIP empaquetada \_ \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ información de MIP empaquetada de CD3DX12 \_ \_ .

</dd> <dt>

**información de \_ MIP empaquetada CD3DX12 explícita \_ \_ (const D3D12 \_ empaquetada de \_ información de MIP \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ información de MIP empaquetada CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de [**\_ \_ \_ información de MIP empaquetada de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

</dd> <dt>

**CD3DX12 \_ \_ información de MIP empaquetada \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**
</dt> <dd>

Crea una nueva instancia de una \_ información de MIP empaquetada CD3DX12 \_ \_ , inicializando los siguientes parámetros:

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**operador const D3D12 \_ empaquetado de la \_ información de MIP \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ \_ información de MIP empaquetada \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





