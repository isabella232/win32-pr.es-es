---
description: Confirme los cambios realizados en una malla en el dispositivo para que se puedan representar. Se debe llamar a esto después de modificar los datos de una malla y antes de representarse. Una malla no se puede representar a menos que se haya confirmado en el dispositivo. Vea Notas.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: Método ID3DX10Mesh::CommitToDevice (D3DX10.h)
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
ms.openlocfilehash: 50dde79e57ca7edf838f05b1fa1b4d10f5da5cc936b3cbf563c7838703650806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567035"
---
# <a name="id3dx10meshcommittodevice-method"></a>Método ID3DX10Mesh::CommitToDevice

Confirme los cambios realizados en una malla en el dispositivo para que se puedan representar. Se debe llamar a esto después de modificar los datos de una malla y antes de representarse. Una malla no se puede representar a menos que se haya confirmado en el dispositivo. Vea Notas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Cuando se carga una malla, los datos se cargan en recursos de almacenamiento provisional, lo que significa que los datos se pueden modificar pero no representar. Cuando se llama a CommitToDevice, los datos de los recursos de almacenamiento provisional se copian en los recursos del dispositivo para que se puedan representar. Aunque los datos se confirman en el dispositivo, los recursos de almacenamiento provisional permanecen y se pueden modificar. Si se realizan modificaciones en los recursos de almacenamiento provisional, los recursos de almacenamiento provisional deben volver a estar confirmados en el dispositivo para que esos cambios se represente en pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




