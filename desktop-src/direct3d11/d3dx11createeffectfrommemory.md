---
title: Función D3DX11CreateEffectFromMemory (D3dx11effect.h)
description: Crea un efecto a partir de un archivo o efecto binario.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Función D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566264"
---
# <a name="d3dx11createeffectfrommemory-function"></a>Función D3DX11CreateEffectFromMemory

Crea un efecto a partir de un archivo o efecto binario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **\* void**

Blob de datos de efecto compilados.

</dd> <dt>

*DataLength* 
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Longitud del blob de datos.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

No existen marcas de efecto. Establecer en cero.

</dd> <dt>

*pDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Puntero al [**id. 3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) en el que se crean los recursos de efecto.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Dirección de la interfaz [**ID3DX11Effect**](id3dx11effect.md) recién creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> Debe usar el [origen De efectos 11 para](https://github.com/Microsoft/FX11) compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de Efectos 11](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

