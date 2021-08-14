---
description: Se produce cuando el usuario suelta una clave mientras el control InkEdit tiene el foco.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Evento InkEdit.KeyUp (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ac908202a22fc1f564c3f21da4cc3cce2e79e2f093ec93b65ff56066f94510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220787"
---
# <a name="inkeditkeyup-event"></a>Evento InkEdit.KeyUp

Se produce cuando el usuario suelta una clave mientras el control [InkEdit](inkedit-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KeyUp(
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

Miembro de la [**enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica qué teclas modificadoras están deprimidas en el momento del evento.



| Valor                                                                                                                                                                                     | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**Desplazamiento \_ IKM**</dt> </dl>             | Especifica que la tecla MAYÚS se usó como modificador. <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_ Control**</dt> </dl> | Especifica que la tecla CTRL se usó como modificador. <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_ Alt**</dt> </dl>                 | Especifica que la tecla ALT se usó como modificador. <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este evento se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeKeyUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada manuscrita)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Control InkEdit del \[ evento KeyDown\]**](inkedit-keydown.md)
</dt> <dt>

[**Control InkEdit del \[ evento KeyPress\]**](inkedit-keypress.md)
</dt> </dl>

 

