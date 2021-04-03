---
description: La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaz ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083816"
---
# <a name="id3dxline-interface"></a>Interfaz ID3DXLine

La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.

## <a name="members"></a>Miembros

La interfaz **ID3DXLine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXLine** tiene estos métodos.



| Método                                                | Descripción                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dxline--begin.md)                     | Prepara un dispositivo para dibujar líneas.<br/>                                                                                                                                                  |
| [**Dibujar**](id3dxline--draw.md)                       | Dibuja una franja de líneas en el espacio de la pantalla. La entrada está en forma de una matriz que define los puntos (de [**D3DXVECTOR2**](d3dxvector2.md)) en la franja de línea.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Dibuja una franja de líneas en el espacio de la pantalla con una matriz de transformación de entrada especificada.<br/>                                                                                                      |
| [**Fin**](id3dxline--end.md)                         | Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a [**ID3DXLine:: Begin**](id3dxline--begin.md) .<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Obtiene el estado de suavizado de línea.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera el dispositivo Direct3D asociado al objeto de línea.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Obtiene el modo de dibujo de líneas de estilo OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Obtiene el patrón punteado de línea.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Obtiene el valor de escala del patrón punteado.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Obtiene el grosor de la línea.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Alterna el suavizado de contorno de línea.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Alterna el modo para dibujar líneas de estilo OpenGL.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Aplica un patrón punteado a la línea.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Estira el patrón punteado a lo largo de la dirección de la línea.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Especifica el grosor de la línea.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Observaciones

Cree un objeto de dibujo de línea con [**D3DXCreateLine**](d3dxcreateline.md).

El tipo LPD3DXLINE se define como un puntero a la interfaz **ID3DXLine** .


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
