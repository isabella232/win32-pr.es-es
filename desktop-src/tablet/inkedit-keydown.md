---
description: Se produce cuando el usuario presiona una tecla mientras el control InkEdit tiene el foco.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit.KeyDown (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ab1c1b54f9f60d4bd0868f6e093505e21255991502653712a540728394664c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967144"
---
# <a name="inkeditkeydown-event"></a>InkEdit.KeyDown, evento

Se produce cuando el usuario presiona una tecla mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pkey* 
</dt> <dd>

Código de clave virtual de la tecla presionada por el usuario.

</dd> <dt>

*MayúsKey* 
</dt> <dd>

Miembro de la [**enumeración InkShiftKeyModifierFlags,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras se deprimen en el momento del evento.



| Value                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Desplazamiento \_ de IKM**</dt> </dl>             | Especifica que la tecla MAYÚS se usó como modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Control**</dt> </dl> | Especifica que la tecla CTRL se usó como modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que la tecla ALT se usó como modificador. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyDown.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada de lápiz)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyPress Event \[ InkEdit Control\]**](inkedit-keypress.md)
</dt> <dt>

[**KeyUp Event \[ InkEdit Control\]**](inkedit-keyup.md)
</dt> </dl>

 

