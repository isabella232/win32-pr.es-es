---
description: Notifica a una aplicación cuando un IME está a punto de abrir la ventana candidata. La aplicación recibe este comando a través del mensaje \_ WM IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 439ff125-2731-4eb1-8287-4ca8ace7d8ec
title: IMN_OPENCANDIDATE evento (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf6db7415a62b6d77925a4fb7106b70f0b42d77f922e0c1b6df76e71d10c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147638"
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

Marca de lista de candidatos. Cada bit corresponde a una lista candidata: bit 0 a la primera lista, bit 1 al segundo, y así sucesivamente. Si un bit especificado es 1, la ventana candidata correspondiente está a punto de abrirse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Una aplicación debe procesar este comando si muestra los propios candidatos. La aplicación puede recuperar una lista de candidatos para mostrar mediante la función [**ImmGetCandidateList.**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

De forma predeterminada, la ventana de IME crea una ventana candidata cuando procesa este comando.

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

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




