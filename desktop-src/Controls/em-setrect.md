---
title: EM_SETRECT mensaje (Winuser.h)
description: 'EM_SETRECT mensaje: establece el rectángulo de formato de un control de edición multilínea.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062072"
---
# <a name="em_setrect-message"></a>Mensaje \_ DE EM SETRECT

Establece el [rectángulo de formato de](about-edit-controls.md) un control de edición multilínea. El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.

Este mensaje solo se procesa mediante controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2.0 y versiones posteriores:** Indica si *lParam especifica* coordenadas absolutas o relativas. Un valor de cero indica coordenadas absolutas. Un valor de 1 indica desplazamientos relativos al rectángulo de formato actual. (Los desplazamientos pueden ser positivos o negativos).

**Editar controles y Rich Edit 1.0:** Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo. Si este parámetro es **NULL,** el rectángulo de formato se establece en sus valores predeterminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Establecer *lParam* en **NULL** no tiene ningún efecto si se instala un dispositivo táctil o si **EM \_ SETRECT** se envía desde un subproceso que tiene un enlace instalado (vea [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). En estos casos, *lParam* debe contener un puntero válido a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85))

El **mensaje \_ EM SETRECT** hace que se vuelva a dibujar el texto del control de edición. Para cambiar el tamaño del rectángulo de formato sin volver a dibujar el texto, use el mensaje [**\_ EM SETRECTNP.**](em-setrectnp.md)

Cuando se crea por primera vez un control de edición, el rectángulo de formato se establece en un tamaño predeterminado. Puede usar el mensaje **\_ SETRECT** de EM para que el rectángulo de formato sea mayor o menor que la ventana de control de edición.

Si el control de edición no tiene una barra de desplazamiento horizontal y el rectángulo de formato está establecido en mayor que la ventana de control de edición, las líneas de texto que superan el ancho de la ventana de control de edición (pero más pequeñas que el ancho del rectángulo de formato) se recortan en lugar de ajustarse.

Si el control de edición contiene un borde, el tamaño del borde reduce el rectángulo de formato. Si va a ajustar el rectángulo devuelto por un mensaje [**EM \_ GETRECT,**](em-getrect.md) debe quitar el tamaño del borde antes de usar el rectángulo con el mensaje **EM \_ SETRECT.**

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. El rectángulo de formato no incluye la barra de selección, que es un área sin marca a la izquierda de cada párrafo. Cuando el usuario hace clic en la barra de selección, se selecciona la línea correspondiente. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETRECT**](em-getrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

