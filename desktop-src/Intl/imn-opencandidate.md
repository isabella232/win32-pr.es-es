---
description: Notifica a una aplicación cuando un IME está a punto de abrir la ventana candidata. La aplicación recibe este comando a través del mensaje \_ WM IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: IMN_OPENCANDIDATE evento (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f8f412c60cc6b62904e562d450479af642de0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063117"
---
# <a name="imn_opencandidate-event"></a>Evento \_ OPENCANDIDATE de IMN

Notifica a una aplicación cuando un IME está a punto de abrir la ventana candidata. La aplicación recibe este comando a través del mensaje [**\_ WM IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_OPENCANDIDATE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ OPENCANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 al segundo, y así sucesivamente. Si un bit especificado es 1, la ventana candidata correspondiente está a punto de abrirse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este comando si muestra los candidatos. La aplicación puede recuperar una lista de candidatos para mostrar mediante la [**función ImmGetCandidateList.**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

De forma predeterminada, la ventana IME crea una ventana candidata cuando procesa este comando.

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

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




