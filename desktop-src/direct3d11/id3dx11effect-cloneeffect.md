---
title: Método ID3DX11Effect CloneEffect (D3dx11effect.h)
description: Crea una copia de una interfaz de efecto.
ms.assetid: 98cc8e25-38c5-4b87-99eb-39d2edd9053c
keywords:
- Método CloneEffect Direct3D 11
- Método CloneEffect Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método CloneEffect
topic_type:
- apiref
api_name:
- ID3DX11Effect.CloneEffect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dc7e47d1c50d0e41c29c90102afaaebdce8dda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966907"
---
# <a name="id3dx11effectcloneeffect-method"></a>Método ID3DX11Effect::CloneEffect

Crea una copia de una interfaz de efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneEffect(
   UINT          Flags,
   ID3DX11Effect **ppClonedEffect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Marcas que afectan a la creación del efecto clonado. Puede ser 0 o uno de los valores siguientes.



| Marca                                    | Descripción                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX11 \_ EFFECT \_ CLONE \_ FORCE \_ NONSINGLE | Omitir todos los calificadores "únicos" en los búferes. Todos los cbuffers tendrán sus propios [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)creados en el efecto clonado. |



 

</dd> <dt>

*ppClonedEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Puntero a un [**puntero ID3DX11Effect**](id3dx11effect.md) que se establecerá en la copia del efecto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

