---
description: Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con los parámetros establecidos como se muestra a continuación.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: Código de notificación de IMR_DOCUMENTFEED (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276728"
---
# <a name="imr_documentfeed-notification-code"></a>Código de notificación de IMR \_ DOCUMENTFEED

Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con los parámetros establecidos como se muestra a continuación.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a un búfer que va a contener la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la estructura de la cadena de reconversión actual. Si *lParam* se establece en **null**, la aplicación devuelve el tamaño necesario para que el búfer contenga la estructura. El comando devuelve 0 si no se realiza correctamente.

## <a name="remarks"></a>Observaciones

El IME almacena en caché las cadenas convertidas para una mayor precisión de la conversión. Una limitación del almacenamiento en caché del IME es que pierde la cadena convertida en las siguientes circunstancias:

-   La posición del símbolo de intercalación para la aplicación se mueve mediante una clave, por ejemplo, una tecla de cursor.
-   La posición del símbolo de intercalación para la aplicación se mueve por el mouse.
-   Se abre un nuevo documento.

Con el comando **IMR \_ DOCUMENTFEED** , el IME puede actualizar las cadenas almacenadas en caché en cualquier momento. El uso de este comando mejora la precisión de la conversión.

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

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




