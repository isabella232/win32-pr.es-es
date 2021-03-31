---
description: Cree una vista de recursos del sombreador desde un archivo en la memoria.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: Función D3DX10CreateShaderResourceViewFromMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820986"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a>D3DX10CreateShaderResourceViewFromMemory función)

Cree una vista de recursos del sombreador desde un archivo en la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará el recurso.

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al archivo en memoria que contiene la vista de recursos del sombreador.

</dd> <dt>

*SrcDataSize* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**

Tamaño del archivo en memoria.

</dd> <dt>

*pLoadInfo* \[ de\]
</dt> <dd>

Tipo: **[ **\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)\***

Opcional. Identifica las características de una textura (consulte [**\_ información de \_ carga \_ de imagen de D3DX10**](d3dx10-image-load-info.md)) cuando se crea el procesador de datos; establezca este valor en **null** para leer las características de una textura cuando se carga la textura.

</dd> <dt>

*pPump* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)). Si se especifica **null** , esta función se comportará de forma sincrónica y no volverá hasta que finalice.

</dd> <dt>

*ppShaderResourceView* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Dirección de un puntero a la vista de recursos del sombreador recién creada. Consulte la [**interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

*pHResult* \[ enuncia\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**. Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
