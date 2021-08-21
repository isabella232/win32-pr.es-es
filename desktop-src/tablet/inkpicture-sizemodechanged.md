---
description: Se produce después de cambiar la propiedad SizeMode del control InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture.SizeModeChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebcd5a659894c6f70a87ea75f7a99321d94dba2826fd538530f7e6d060d5730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032033"
---
# <a name="inkpicturesizemodechanged-event"></a>Evento InkPicture.SizeModeChanged

Se produce después de cambiar la propiedad [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) del control [InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewMode* \[ En\]
</dt> <dd>

Nuevo estado del control [InkPicture,](inkpicture-control-reference.md) basado en el nuevo valor de la [**propiedad SizeMode.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> <dt>

*OldMode* \[ En\]
</dt> <dd>

Estado anterior del control [InkPicture,](inkpicture-control-reference.md) basado en el valor anterior de la [**propiedad SizeMode.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPESizeModeChanged.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

