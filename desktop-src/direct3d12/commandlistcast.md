---
title: Función CommandListCast (D3dx12.h)
description: Esta plantilla de función convierte un puntero constante a cualquier lista de comandos en un puntero const a id3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Función CommandListCast
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570909"
---
# <a name="commandlistcast-function"></a>Función CommandListCast

Esta plantilla de función convierte un puntero constante a cualquier lista de comandos en un puntero const a id3D12CommandList.

Esta conversión es útil para pasar punteros de lista de comandos fuertemente tipos a [**ExecuteCommandLists.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)

## <a name="syntax"></a>Sintaxis


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pp* 
</dt> <dd>

Tipo: **t \_ CommandListType \* const \***

Lista de comandos fuertemente tipos que se convierten.

El argumento de **plantilla t \_ CommandListType** especifica cualquier objeto de lista de comandos fuertemente escrito.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **ID3D12CommandList \* const \***

Lista de comandos fuertemente tipos, reinterpretada como [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).

## <a name="remarks"></a>Observaciones

CommandListCast realiza una **conversión reinterpretación. \_** La conversión es válida siempre que se respete la const-ness de la lista de comandos.

La función CommandListCast se define de la siguiente manera:


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





