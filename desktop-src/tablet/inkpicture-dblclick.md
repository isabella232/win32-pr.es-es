---
description: Se produce cuando se hace doble clic en el control InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture.DblClick (Ms inkut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 515d16d16fb585771a8e2e06e642476b6be7a29851b750add4d6de2ca1a89bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717334"
---
# <a name="inkpicturedblclick-event"></a>Evento InkPicture.DblClick

Se produce cuando se hace doble clic en el control [InkPicture.](inkpicture-control-reference.md)

## <a name="syntax"></a>Sintaxis


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Si el evento se debe cancelar para el control primario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para distinguir entre los botones izquierdo, derecho y central del mouse, use los eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp.**](inkpicture-mouseup.md) Si hay código en el evento [**Click,**](inkpicture-click.md) el **evento DblClick** nunca se desencadenará.

 

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEDblClick**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




