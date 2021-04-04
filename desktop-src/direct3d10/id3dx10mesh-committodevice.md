---
description: Confirme los cambios realizados en una malla en el dispositivo para que los cambios se puedan representar. Se debe llamar a este método después de que se modifiquen los datos de una malla y antes de que se representen. No se puede representar una malla a menos que se confirme en el dispositivo. Vea Notas.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh:: CommitToDevice (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083734"
---
# <a name="id3dx10meshcommittodevice-method"></a>ID3DX10Mesh:: CommitToDevice (método)

Confirme los cambios realizados en una malla en el dispositivo para que los cambios se puedan representar. Se debe llamar a este método después de que se modifiquen los datos de una malla y antes de que se representen. No se puede representar una malla a menos que se confirme en el dispositivo. Vea Notas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Cuando se carga una malla, se cargan los datos en los recursos de almacenamiento provisional, lo que significa que los datos se pueden modificar pero no se representan. Cuando se llama a CommitToDevice, los datos de los recursos de almacenamiento provisional se copian en recursos de dispositivo para que se puedan representar. Aunque los datos se confirman en el dispositivo, los recursos de almacenamiento provisional permanecen y se pueden modificar. Si se realizan modificaciones en los recursos de almacenamiento provisional, los recursos de almacenamiento provisional deben volver a confirmarse en el dispositivo para que esos cambios se representen en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




