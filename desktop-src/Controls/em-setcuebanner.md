---
title: Mensaje de EM_SETCUEBANNER (commctrl. h)
description: Establece la indicación de texto o la sugerencia que se muestra en el control de edición para solicitar información al usuario.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492467"
---
# <a name="em_setcuebanner-message"></a>\_Mensaje SETCUEBANNER em

Establece la indicación de texto o la sugerencia que se muestra en el control de edición para solicitar información al usuario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

**True** si el banner de indicación debe aparecer incluso cuando el control de edición tiene el foco. en caso contrario, **false**. **False** es el comportamiento predeterminado que desaparece el banner de indicación cuando el usuario hace clic en el control.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el texto que se va a mostrar como indicación textual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **true**. En caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

Un control de edición que se usa para iniciar una búsqueda puede mostrar "Escriba aquí la búsqueda" en el texto gris como una indicación textual. Cuando el usuario hace clic en el texto, el texto desaparece y el usuario puede escribir.

No se puede establecer un banner de indicación en un control de edición multilínea o en un control Rich Edit.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Editar \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





