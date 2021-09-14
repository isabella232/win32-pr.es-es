---
description: Se usa para establecer y consultar efectos, y para elegir técnicas. Un objeto de efecto puede contener varias técnicas para representar el mismo efecto.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interfaz ID3DXEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964772"
---
# <a name="id3dxeffect-interface"></a>Interfaz ID3DXEffect

Se usa para establecer y consultar efectos, y para elegir técnicas. Un objeto de efecto puede contener varias técnicas para representar el mismo efecto.

## <a name="members"></a>Members

La **interfaz ID3DXEffect** hereda de [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXEffect** tiene estos métodos.



| Método                                                                | Descripción                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Aplique los valores de un bloque de estado al estado del sistema de efecto actual.<br/>                                                                                                                 |
| [**Comenzar**](id3dxeffect--begin.md)                                   | Inicia una técnica activa.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Empiece a capturar los cambios de estado en un bloque de parámetros.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Comienza un paso, dentro de la técnica activa.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Crea una copia de un efecto.<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | Propagar los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Elimina un bloque de parámetros.<br/>                                                                                                                                                             |
| [**Final**](id3dxeffect--end.md)                                       | Finaliza una técnica activa.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Detenga la captura de los cambios de estado de los parámetros de efecto.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Finalizar un paso activo.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Busca la siguiente técnica válida, empezando por la técnica después de la técnica especificada.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Obtiene la técnica actual.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Recupera el dispositivo asociado al efecto.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Obtiene un puntero al grupo de parámetros compartidos.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Obtiene el administrador de estado del efecto.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Determina si la técnica usa un parámetro.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Establezca un intervalo contiguo de constantes de sombreador con una copia de memoria.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | Establezca el administrador de estado de efecto.<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | Establece la técnica activa.<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | Validar una técnica.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

La interfaz ID3DXEffect se obtiene llamando a [**D3DXCreateEffect,**](d3dxcreateeffect.md) [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)o [**D3DXCreateEffectFromResource.**](d3dxcreateeffectfromresource.md)

El tipo LPD3DXEFFECT se define como un puntero a esta interfaz.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces de efecto](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




