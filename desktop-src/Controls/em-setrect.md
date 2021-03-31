---
title: Mensaje de EM_SETRECT (Winuser. h)
description: Establece el rectángulo de formato de un control de edición multilínea.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT controles de mensajes de Windows
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
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079309"
---
# <a name="em_setrect-message"></a>\_Mensaje SETRECT em

Establece el [rectángulo de formato](about-edit-controls.md) de un control de edición multilínea. El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.

Este mensaje solo lo procesan los controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edición enriquecida 2,0 y versiones posteriores:** Indica si *lParam* especifica coordenadas absolutas o relativas. Un valor de cero indica coordenadas absolutas. Un valor de 1 indica desplazamientos respecto al rectángulo de formato actual. (Los desplazamientos pueden ser positivos o negativos).

**Controles de edición y edición enriquecida 1,0:** Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo. Si este parámetro es **null**, el rectángulo de formato se establece en sus valores predeterminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se establece *lParam* en **null** , no se produce ningún efecto si se instala un dispositivo táctil o si **em \_ SETRECT** se envía desde un subproceso que tiene un enlace instalado (vea [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). En estos casos, *lParam* debe contener un puntero válido a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) .

El **mensaje \_ SETRECT em** hace que se vuelva a dibujar el texto del control de edición. Para cambiar el tamaño del rectángulo de formato sin volver a dibujar el texto, use el mensaje [**\_ SETRECTNP em**](em-setrectnp.md) .

Cuando se crea un control de edición por primera vez, el rectángulo de formato se establece en un tamaño predeterminado. Puede usar el mensaje **\_ SETRECT em** para que el rectángulo de formato sea más grande o más pequeño que la ventana de control de edición.

Si el control de edición no tiene una barra de desplazamiento horizontal y el rectángulo de formato se establece en un valor mayor que la ventana de control de edición, las líneas de texto que superen el ancho de la ventana de control de edición (pero menor que el ancho del rectángulo de formato) se recortan en lugar de ajustarse.

Si el control de edición contiene un borde, el rectángulo de formato se reduce con el tamaño del borde. Si está ajustando el rectángulo devuelto por un mensaje [**\_ GETRECT em**](em-getrect.md) , debe quitar el tamaño del borde antes de usar el rectángulo con el **mensaje \_ SETRECT em** .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. El rectángulo de formato no incluye la barra de selección, que es un área no marcada a la izquierda de cada párrafo. Cuando el usuario hace clic en la barra de selección, se selecciona la línea correspondiente. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETRECT em**](em-getrect.md)
</dt> <dt>

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

