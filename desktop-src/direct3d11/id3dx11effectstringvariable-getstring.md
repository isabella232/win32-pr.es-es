---
title: Método ID3DX11EffectStringVariable GetString (D3dx11effect.h)
description: Obtenga la cadena.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Método GetString Direct3D 11
- Método GetString Direct3D 11, interfaz ID3DX11EffectStringVariable
- Interfaz ID3DX11EffectStringVariable Direct3D 11, método GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edef49fd0965e06693fb995434c0579080f1e6243522ca4ea1489dedb791f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533003"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a>Método ID3DX11EffectStringVariable::GetString

Obtenga la cadena.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppString* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Puntero a la cadena.

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

 

