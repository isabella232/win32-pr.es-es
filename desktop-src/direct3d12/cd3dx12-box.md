---
title: CD3DX12_BOX estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura BOX D3D12. \_
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- CD3DX12_BOX estructura
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: f2aa358d8b2d772d45c6387221dd9e660a9630fbf90535ada7dcceefc3257879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851415"
---
# <a name="cd3dx12_box-structure"></a>Cd3DX12 \_ (estructura BOX)

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ BOX D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ BOX()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un cuadro CD3DX12. \_

</dd> <dt>

**explicit CD3DX12 \_ BOX(const D3D12 \_ BOX& o)**
</dt> <dd>

Crea una nueva instancia de un cuadro CD3DX12, inicializado con el contenido de otra estructura \_ [**BOX D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Right)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 \_ BOX, inicializando los parámetros siguientes:

LONG Left

LONG Right

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 \_ BOX, inicializando los parámetros siguientes:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**explicit CD3DX12 \_ BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**
</dt> <dd>

Crea una nueva instancia de UN CD3DX12 \_ BOX, inicializando los parámetros siguientes:

LONG Left

LONG Top

LONG Front

LONG Right

LONG Bottom

LONG Back

</dd> <dt>

**~CD3DX12 \_ BOX()**
</dt> <dd>

Destruye una instancia de UN CD3DX12 \_ BOX.

</dd> <dt>

**operator const D3D12 \_ BOX&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





