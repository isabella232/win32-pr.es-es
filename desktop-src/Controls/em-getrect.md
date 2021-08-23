---
title: EM_GETRECT mensaje (Winuser.h)
description: Obtiene el rectángulo de formato de un control de edición.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541045"
---
# <a name="em_getrect-message"></a>Mensaje \_ EM GETRECT

Obtiene el [rectángulo de formato](about-edit-controls.md) de un control de edición. El rectángulo de formato es el rectángulo delimitador en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo de formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto no es significativo.

## <a name="remarks"></a>Comentarios

Puede modificar el rectángulo de formato de un control de edición multilínea mediante los mensajes [**EM \_ SETRECT**](em-setrect.md) y [**EM \_ SETRECTNP.**](em-setrectnp.md)

En determinadas condiciones, **EM \_ GETRECT** podría no devolver los valores exactos que [**EM \_ SETRECT**](em-setrect.md) o [**EM \_ SETRECTNP**](em-setrectnp.md) establecen que será aproximadamente correcto, pero puede estar desactivado en unos pocos píxeles.

**Edición enriqueceda:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. El rectángulo de formato no incluye la barra de selección, que es un área sin marca a la izquierda de cada párrafo. Cuando se hace clic en ella, la barra de selección selecciona la línea. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

