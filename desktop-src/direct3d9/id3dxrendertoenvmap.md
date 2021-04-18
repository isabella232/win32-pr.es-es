---
description: La interfaz ID3DXRenderToEnvMap se usa para generalizar el proceso de representación de mapas de entorno.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interfaz ID3DXRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649452"
---
# <a name="id3dxrendertoenvmap-interface"></a>Interfaz ID3DXRenderToEnvMap

La interfaz ID3DXRenderToEnvMap se usa para generalizar el proceso de representación de mapas de entorno.

## <a name="members"></a>Miembros

La interfaz **ID3DXRenderToEnvMap** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToEnvMap** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXRenderToEnvMap** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | Inicie la representación de un mapa de entorno cúbico.<br/>                                                                                                                                    |
| [**BeginHemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | Inicie la representación de un mapa de entorno de Hemispheric.<br/>                                                                                                                              |
| [**BeginParabolic**](id3dxrendertoenvmap--beginparabolic.md)   | Inicie la representación de un mapa de entorno de parabólica.<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | Inicie la representación de un mapa de entorno esférico.<br/>                                                                                                                                |
| [**Fin**](id3dxrendertoenvmap--end.md)                         | Restaure todos los destinos de representación y, si es necesario, componga todas las caras representadas en la superficie del mapa del entorno.<br/>                                                                           |
| [**Face**](id3dxrendertoenvmap--face.md)                       | Inicia el dibujo de cada una de las caras de un mapa de entorno.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Recupera la descripción de la superficie de representación.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Recupera el dispositivo Direct3D asociado a la asignación de entorno.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Un mapa de entorno se usa para la geometría de la escena de mapa de textura con el fin de proporcionar una escena más sofisticada sin usar geometría compleja. Esta interfaz permite crear superficies para los siguientes tipos de geometría: Cube, Half Sphere o Hemispheric, parabólica o Sphere.

La interfaz **ID3DXRenderToEnvMap** se obtiene mediante una llamada a la función [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) .

El tipo LPD3DXRenderToEnvMap se define como un puntero a la interfaz **ID3DXRenderToEnvMap** .


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
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

 

 
