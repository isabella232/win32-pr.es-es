---
description: La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaz ID3DXLine (D3dx9core.h)
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
ms.openlocfilehash: a9677ca802a800624b374212c6942ab6676423f8d63e62cbf136a8b9e69c533d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951375"
---
# <a name="id3dxline-interface"></a>Interfaz ID3DXLine

La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.

## <a name="members"></a>Miembros

La **interfaz ID3DXLine** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXLine** tiene estos métodos.



| Método                                                | Descripción                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dxline--begin.md)                     | Prepara un dispositivo para dibujar líneas.<br/>                                                                                                                                                  |
| [**Dibujar**](id3dxline--draw.md)                       | Dibuja una franja de líneas en el espacio de la pantalla. La entrada tiene el formato de una matriz que define puntos [**(de D3DXVECTOR2)**](d3dxvector2.md)en la franja de líneas.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Dibuja una franja de líneas en el espacio de pantalla con una matriz de transformación de entrada especificada.<br/>                                                                                                      |
| [**End**](id3dxline--end.md)                         | Restaura el estado del dispositivo a la forma en que estaba cuando se llamó a [**ID3DXLine::Begin.**](id3dxline--begin.md)<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Obtiene el estado de suavizado de contorno de línea.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera el dispositivo Direct3D asociado al objeto de línea.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Obtiene el modo de dibujo de línea de estilo OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Obtiene el patrón de stipple de línea.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Obtiene el valor de escala del patrón de stipple.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Obtiene el grosor de la línea.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Alterna el suavizado de contorno de línea.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Alterna el modo para dibujar líneas de estilo OpenGL.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Aplica un patrón detippla a la línea.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Extiende el patrón detippla a lo largo de la dirección de la línea.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Especifica el grosor de la línea.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Comentarios

Cree un objeto de dibujo de línea [**con D3DXCreateLine**](d3dxcreateline.md).

El tipo LPD3DXLINE se define como un puntero a la **interfaz ID3DXLine.**


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
