---
title: Interfaz ID3DX11EffectType (D3dx11effect.h)
description: La interfaz ID3DX11EffectType tiene acceso a las variables de efecto por tipo. La duración de un objeto ID3DX11EffectType es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interfaz ID3DX11EffectType direct3D 11
- Interfaz ID3DX11EffectType Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465756"
---
# <a name="id3dx11effecttype-interface"></a>Interfaz ID3DX11EffectType

La **interfaz ID3DX11EffectType** tiene acceso a las variables de efecto por tipo.

La duración de **un objeto ID3DX11EffectType** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectType** tiene estos métodos.



| Método                                                                       | Descripción                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Obtiene una descripción del tipo de efecto.<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | Obtiene el nombre de un miembro.<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | Obtiene la semántica adjunta a un miembro.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Obtiene un tipo de miembro por índice.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Obtenga un tipo de miembro por nombre.<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Obtiene un tipo de miembro por semántica.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Comprueba que el tipo de efecto es válido.<br/>   |



 

## <a name="remarks"></a>Observaciones

Para obtener información sobre un tipo de efecto de una variable de efecto, llame a [**ID3DX11EffectVariable::GetType**](id3dx11effectvariable-gettype.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





