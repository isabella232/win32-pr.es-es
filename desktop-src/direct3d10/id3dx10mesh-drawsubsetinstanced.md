---
description: Dibuja varias instancias del mismo subconjunto de una malla.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh::D método rawSubsetInstanced (D3DX10. h)
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
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678834"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh::D método rawSubsetInstanced

Dibuja varias instancias del mismo subconjunto de una malla.

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

*AttribId* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifica el subconjunto de la malla que se va a dibujar. Este valor se usa para diferenciar caras en una malla como perteneciente a uno o varios grupos de atributos. Vea Notas.

</dd> <dt>

*InstanceCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de instancias que se van a representar.

</dd> <dt>

*StartInstanceLocation* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

La instancia de en la que se va a iniciar la captura en cada búfer marcado como datos de instancia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Una malla contiene una tabla de atributos. La tabla de atributos puede dividir una malla en subconjuntos, donde cada subconjunto se identifica con un identificador de atributo. Por ejemplo, una malla con 200 caras, dividida en tres subconjuntos, podría tener una tabla de atributos similar a la siguiente:



|            |                 |
|------------|-----------------|
| AttribID 0 | Caras 0 ~ 50    |
| AttribID 1 | Caras 51 ~ 125  |
| AttribID 2 | Caras 126 ~ 200 |



 

La creación de instancias puede ampliar el rendimiento mediante la reutilización de la misma geometría para dibujar varios objetos en una escena. Un ejemplo de creación de instancias podría ser dibujar el mismo objeto con diferentes posiciones y colores. La indexación requiere varios búferes de vértices: al menos uno para los datos por vértice y un segundo búfer para los datos por instancia.

Dibujar instancias con DrawSubsetInstanced es muy similar al proceso utilizado con [**ID3D10Device::D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) que se describe en el ejemplo de [creación de instancias](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx). La diferencia clave al usar DrawSubsetInstanced es que los búferes de vértices y de índices deben extraerse del objeto de [**interfaz ID3DX10Mesh**](id3dx10mesh.md) antes de que se puedan combinar los datos de la instancia.

En el código siguiente se muestra cómo extraer los búferes de vértices y de índices del objeto de malla.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
