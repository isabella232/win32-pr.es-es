---
description: Notifica a una aplicación cuando el IME necesita cambiar la estructura RECONVERTSTRING. La aplicación recibe este comando a través del mensaje WM \_ IME \_ REQUEST con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948802"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>Código de notificación \_ CONFIRMRECONVERTSTRING de IMR

Notifica a una aplicación cuando el IME necesita cambiar la [**estructura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a una [**estructura RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) desde el IME. Para obtener más información, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación acepta la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificada. De lo contrario, el comando devuelve 0 y el IME usa la **estructura RECONVERTSTRING** original.

## <a name="remarks"></a>Comentarios

La aplicación rellena la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) al recibir el comando [ \_ IMR RECONVERTSTRING.](imr-reconvertstring.md)

Después de que la aplicación haya [manipulado IMR \_ RECONVERTSTRING,](imr-reconvertstring.md)el IME podría ajustar o no la [**estructura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) El IME envía LA \_ SOLICITUD DE WM IME con \_ **IMR \_ CONFIRMRECONVERTSTRING** para confirmar los cambios en la **estructura RECONVERTSTRING.** Si la aplicación devuelve **TRUE para** **IMR \_ CONFIRMRECONVERTSTRING,** el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** para el comando **\_ CONFIRMRECONVERTSTRING de IMR.** Si la aplicación devuelve **FALSE** para **\_ IMR CONFIRMRECONVERTSTRING,** el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** original especificada por la aplicación en el comando \_ RECONVERTSTRING de IMR.

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**SOLICITUD \_ DE WM IME \_**](wm-ime-request.md)
</dt> </dl>

 

 




