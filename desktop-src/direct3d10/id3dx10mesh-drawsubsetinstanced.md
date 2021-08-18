---
description: Dibuje varias instancias del mismo subconjunto de una malla.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: Método ID3DX10Mesh::D rawSubsetInstanced (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41da932b5f9445df83c0783b7788b8a7079af2acb74643ea37111d8482e8e208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990435"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>Método ID3DX10Mesh::D rawSubsetInstanced

Dibuje varias instancias del mismo subconjunto de una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AttribId* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifica qué subconjunto de la malla se va a dibujar. Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos. Vea Notas.

</dd> <dt>

*InstanceCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de instancias que se representará.

</dd> <dt>

*StartInstanceLocation* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Instancia de la que se va a empezar a capturar en cada búfer marcado como datos de instancia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Una malla contiene una tabla de atributos. La tabla de atributos puede dividir una malla en subconjuntos, donde cada subconjunto se identifica con un identificador de atributo. Por ejemplo, una malla con 200 caras, dividida en tres subconjuntos, podría tener una tabla de atributos similar a la siguiente:



| Subset     | Caras           |
|------------|-----------------|
| AttribID 0 | Caras 0 ~ 50    |
| AttribID 1 | Caras 51 ~ 125  |
| AttribID 2 | Caras 126 ~ 200 |



 

La creación de instancias puede ampliar el rendimiento si se vuelve a usar la misma geometría para dibujar varios objetos en una escena. Un ejemplo de creación de instancias podría ser dibujar el mismo objeto con diferentes posiciones y colores. La indexación requiere varios búferes de vértices: al menos uno para los datos por vértice y un segundo búfer para los datos por instancia.

Dibujar instancias con DrawSubsetInstanced es muy similar al proceso usado con [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) que se describe en Ejemplo de creación de instancias [.](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx) La diferencia clave al usar DrawSubsetInstanced es que los búferes de vértice e índice deben extraerse del objeto [**ID3DX10Mesh Interface**](id3dx10mesh.md) para poder combinar los datos de creación de instancias.

El código siguiente muestra cómo extraer los búferes de vértice e índice del objeto de malla.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
