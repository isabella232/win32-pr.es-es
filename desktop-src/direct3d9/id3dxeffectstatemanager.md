---
description: Se trata de una interfaz implementada por el usuario que permite a un usuario establecer el estado del dispositivo de un efecto.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interfaz ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362645"
---
# <a name="id3dxeffectstatemanager-interface"></a>Interfaz ID3DXEffectStateManager

Se trata de una interfaz implementada por el usuario que permite a un usuario establecer el estado del dispositivo de un efecto. El usuario debe implementar cada uno de los métodos de esta interfaz y, a continuación, se usarán como devoluciones de llamada a la aplicación cuando se produzca cualquiera de las siguientes situaciones:

-   Un efecto llama a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   El estado del efecto se actualiza dinámicamente mediante una llamada a la API de cambio de estado adecuada. Consulte páginas de método individuales para obtener más información.

Cuando una aplicación utiliza el administrador de estado para implementar devoluciones de llamada personalizadas, un efecto ya no guarda y restaura el estado automáticamente al llamar a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md). Dado que la aplicación ha implementado un comportamiento personalizado de guardar y restaurar en las devoluciones de llamada, se omite este comportamiento automático.

## <a name="members"></a>Miembros

La interfaz **ID3DXEffectStateManager** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXEffectStateManager** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXEffectStateManager** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**LightEnable**](id3dxeffectstatemanager--lightenable.md)                           | Función de devolución de llamada que debe ser implementada por un usuario para habilitar o deshabilitar una luz.<br/>                                 |
| [**SetFVF**](id3dxeffectstatemanager--setfvf.md)                                     | Una función de devolución de llamada que debe ser implementada por un usuario para establecer un código FVF.<br/>                                         |
| [**SetLight**](id3dxeffectstatemanager--setlight.md)                                 | Función de devolución de llamada que debe ser implementada por un usuario para establecer una luz.<br/>                                            |
| [**SetMaterial**](id3dxeffectstatemanager--setmaterial.md)                           | Una función de devolución de llamada que debe ser implementada por un usuario para establecer el estado del material.<br/>                                     |
| [**SetNPatchMode**](id3dxeffectstatemanager--setnpatchmode.md)                       | Una función de devolución de llamada que debe ser implementada por un usuario para establecer el número de segmentos de subdivisión para N-patches.<br/>   |
| [**SetPixelShader**](id3dxeffectstatemanager--setpixelshader.md)                     | Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.<br/>                                     |
| [**SetPixelShaderConstantB**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.<br/>        |
| [**SetPixelShaderConstantF**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.<br/> |
| [**SetPixelShaderConstantI**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.<br/>        |
| [**SetRenderState**](id3dxeffectstatemanager--setrenderstate.md)                     | Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.<br/>                                       |
| [**SetSamplerState**](id3dxeffectstatemanager--setsamplerstate.md)                   | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una muestra.<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | Función de devolución de llamada que debe ser implementada por un usuario para establecer una textura.<br/>                                          |
| [**SetTextureStageState**](id3dxeffectstatemanager--settexturestagestate.md)         | Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una transformación.<br/>                                        |
| [**SetVertexShader**](id3dxeffectstatemanager--setvertexshader.md)                   | Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de vértices.<br/>                                    |
| [**SetVertexShaderConstantB**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.<br/>        |
| [**SetVertexShaderConstantF**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.<br/> |
| [**SetVertexShaderConstantI**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de tipo entero de sombreador de vértices.<br/>        |



 

## <a name="remarks"></a>Observaciones

Un usuario crea una interfaz ID3DXEffectStateManager implementando una clase que deriva de esta interfaz e implementando todos los métodos de interfaz. Una vez creada la interfaz, puede obtener o establecer el administrador de estado dentro de un efecto mediante [**ID3DXEffect:: GetStateManager**](id3dxeffect--getstatemanager.md) y [**ID3DXEffect:: SetStateManager**](id3dxeffect--setstatemanager.md).

El tipo LPD3DXEFFECTSTATEMANAGER se define como un puntero a esta interfaz.


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de efectos](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
