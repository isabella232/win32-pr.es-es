---
description: Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: Código de notificación de IMN_CHANGECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156585"
---
# <a name="imn_changecandidate-notification-code"></a>Código de notificación de CHANGECANDIDATE de IMN \_

Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata. La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establézcalo en IMN \_ CHANGECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a la segunda lista, etc. Si un bit especificado es 1, la ventana candidata correspondiente se va a cambiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este comando si muestra los propios candidatos.

La ventana del IME cambia el aspecto de la ventana candidata al procesar este comando. Una aplicación puede obtener información sobre la ventana del sistema con [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) y [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**\_notificación de IME de WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




