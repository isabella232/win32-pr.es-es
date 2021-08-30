---
title: Método ID3DX11EffectStringVariable GetStringArray (D3dx11effect.h)
description: Obtiene una matriz de cadenas.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Método GetStringArray Direct3D 11
- Método GetStringArray Direct3D 11, interfaz ID3DX11EffectStringVariable
- Interfaz ID3DX11EffectStringVariable Direct3D 11, método GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e88772edef9b975b34287b448b477e5ad2ada5cbf3f5f006dd76b8b9d158c3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894905"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a>Método ID3DX11EffectStringVariable::GetStringArray

Obtiene una matriz de cadenas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppStrings* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Puntero a la primera cadena de la matriz.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Desplazamiento (en número de cadenas) entre el inicio de la matriz y la primera cadena que se obtiene.

</dd> <dt>

*Recuento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Número de cadenas de la matriz devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes códigos [de retorno de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen Effects 11 para compilar la aplicación de tipo effects. Para obtener más información sobre el uso del origen de Efectos 11, vea [Diferencias entre los efectos 10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de efectos 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

