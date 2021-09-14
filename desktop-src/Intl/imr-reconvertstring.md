---
description: Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión. La aplicación recibe este comando a través del mensaje WM \_ IME \_ REQUEST con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063107"
---
# <a name="imr_reconvertstring-notification-code"></a>Código de notificación \_ RECONVERTSTRING de IMR

Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Se establece en IMR \_ RECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a un búfer que contiene la [**estructura RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) y las cadenas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la estructura de cadena de reconversión actual. Si *lParam se* establece en **NULL,** la aplicación devuelve el tamaño del búfer necesario para contener la estructura. El comando devuelve 0 si no se realiza correctamente.

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

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**SOLICITUD \_ DE WM IME \_**](wm-ime-request.md)
</dt> </dl>

 

 




