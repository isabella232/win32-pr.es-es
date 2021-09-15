---
title: Interfaz ID3DX11EffectConstantBuffer (D3dx11effect.h)
description: Una interfaz de búfer constante tiene acceso a búferes constantes o búferes de textura.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465393"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Interfaz ID3DX11EffectConstantBuffer

Una interfaz de búfer constante tiene acceso a búferes constantes o búferes de textura.

## <a name="members"></a>Members

La **interfaz ID3DX11EffectConstantBuffer** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectConstantBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectConstantBuffer** tiene estos métodos.



| Método                                                                             | Descripción                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Obtenga un búfer constante.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Obtiene un búfer de textura.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Establezca un búfer constante.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Establezca un búfer de textura.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Revierte un búfer constante establecido previamente.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Revierte un búfer de textura establecido previamente.<br/>  |



 

## <a name="remarks"></a>Observaciones

Use búferes constantes para almacenar muchas constantes de efecto; agrupar constantes en búferes en función de su frecuencia de actualización. Esto le permite minimizar el número de cambios de estado, así como realizar el menor número de llamadas API para cambiar el estado. Ambos factores conducen a un mejor rendimiento.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





