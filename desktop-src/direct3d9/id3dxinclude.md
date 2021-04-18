---
description: ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para las \# directivas de inclusión durante la compilación del sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaz ID3DXInclude (D3DX9Shader. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708079"
---
# <a name="id3dxinclude-interface"></a>Interfaz ID3DXInclude

ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para las \# directivas de inclusión durante la compilación del sombreador. Cada uno de los métodos de esta interfaz debe ser implementado por el usuario, que se utilizará como devoluciones de llamada para la aplicación cuando se produzca uno de los siguientes casos:

-   Un sombreador HLSL que contiene un \# include se compila mediante una llamada a una de las funciones de D3DXCompileShader \* \* \* .
-   Un sombreador de ensamblado \# incluye el ensamblado llamando a cualquiera de las funciones de D3DXAssembleShader \* \* \* .
-   Un efecto que contiene un \# include se compila mediante una llamada a cualquiera de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .

## <a name="members"></a>Miembros

La interfaz **ID3DXInclude** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXInclude** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXInclude** tiene estos métodos.



| Método                               | Descripción                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Cercanos**](id3dxinclude--close.md) | Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .<br/>                             |
| [**Ábra**](id3dxinclude--open.md)   | Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .<br/> |



 

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
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de efectos](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
