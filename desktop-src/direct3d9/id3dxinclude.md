---
description: ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para \# las directivas include durante la compilación del sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaz ID3DXInclude (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360856"
---
# <a name="id3dxinclude-interface"></a>Interfaz ID3DXInclude

ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para \# las directivas include durante la compilación del sombreador. El usuario debe implementar cada uno de los métodos de esta interfaz, que luego se usará como devoluciones de llamada a la aplicación cuando se produzca una de las siguientes situaciones:

-   Un sombreador HLSL que contiene una include se compila mediante una llamada a \# una de las funciones D3DXCompileShader. \* \* \*
-   Una función de sombreador de ensamblados se ensambla mediante una llamada a cualquiera de las funciones \# D3DXAssembleShader. \* \* \*
-   Un efecto que contiene un include se compila mediante una llamada a cualquiera de las funciones \# D3DXCreateEffect o \* \* \* D3DXCreateEffectCompiler. \* \* \*

## <a name="members"></a>Members

La **interfaz ID3DXInclude** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXInclude** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXInclude** tiene estos métodos.



| Método                               | Descripción                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Cerca**](id3dxinclude--close.md) | Método implementado por el usuario para cerrar un archivo de incluir \# sombreador.<br/>                             |
| [**Abrir**](id3dxinclude--open.md)   | Método implementado por el usuario para abrir y leer el contenido de un archivo de contenido \# de sombreador.<br/> |



 

## <a name="remarks"></a>Observaciones

Un usuario crea una interfaz ID3DXInclude implementando una clase que deriva de esta interfaz e implementando todos los métodos de interfaz.

El tipo LPD3DXINCLUDE se define como un puntero a esta interfaz.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Interfaces de efecto](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
