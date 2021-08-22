---
description: Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata. La aplicación recibe este comando a través del mensaje WM \_ IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599f064b05f4fa0bda205825d623d13eec39334683fbe2b69f1c8b7b2997026b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949256"
---
# <a name="imn_changecandidate-notification-code"></a>Código de notificación \_ CHANGECANDIDATE de IMN

Notifica a la aplicación cuando un IME está a punto de cambiar el contenido de la ventana candidata. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ CHANGECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista candidata: bit 0 a la primera lista, bit 1 a la segunda lista, y así sucesivamente. Si un bit especificado es 1, la ventana candidata correspondiente está a punto de cambiarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Una aplicación debe procesar este comando si muestra los propios candidatos.

La ventana IME cambia la apariencia de la ventana candidata cuando procesa este comando. Una aplicación puede obtener información sobre la ventana del sistema con [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) e [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




