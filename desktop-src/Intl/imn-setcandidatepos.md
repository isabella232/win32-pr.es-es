---
description: Notifica a una aplicación cuando el procesamiento de candidatos ha finalizado y el IME está a punto de mover la ventana candidata. La aplicación recibe este comando a través del mensaje \_ WM IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063114"
---
# <a name="imn_setcandidatepos-notification-code"></a>Código de \_ notificación DE IMN SETCANDIDATEPOS

Notifica a una aplicación cuando el procesamiento de candidatos ha finalizado y el IME está a punto de mover la ventana candidata. La aplicación recibe este comando a través del mensaje [**\_ WM IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 al segundo, y así sucesivamente. Si un bit especificado es 1, la ventana candidata correspondiente está a punto de moverse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este comando si muestra la propia ventana candidata.

La ventana IME mueve la ventana candidata cuando procesa este comando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




