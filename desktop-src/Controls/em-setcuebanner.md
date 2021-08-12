---
title: EM_SETCUEBANNER mensaje (Commctrl.h)
description: Establece la indicación textual, o sugerencia, que muestra el control de edición para solicitar información al usuario.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SETCUEBANNER controles de Windows mensaje
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
ms.openlocfilehash: b08694d7368a994c639f236f18537e13d81f57083521599c23671941c74889bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673108"
---
# <a name="em_setcuebanner-message"></a>Mensaje \_ EM SETCUEBANNER

Establece la indicación textual, o sugerencia, que muestra el control de edición para solicitar información al usuario.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

**TRUE** si el banner de la indicación debe mostrarse incluso cuando el control de edición tiene el foco; de lo contrario, **FALSE**. **FALSE** es el comportamiento predeterminado que el banner de indicación desaparece cuando el usuario hace clic en el control.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el texto que se mostrará como la indicación textual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Observaciones

Un control de edición que se usa para iniciar una búsqueda puede mostrar "Entrar búsqueda aquí" en texto gris como una indicación textual. Cuando el usuario hace clic en el texto, el texto desaparece y el usuario puede escribirlo.

No se puede establecer un banner de indicación en un control de edición multilínea o en un control de edición enriquecido.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Editar \_ SetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





