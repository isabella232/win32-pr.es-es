---
description: Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación. La aplicación recibe este comando a través del mensaje WM \_ IME \_ REQUEST con parámetros establecidos como se muestra a continuación.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063109"
---
# <a name="imr_documentfeed-notification-code"></a>Código de \_ notificación DE IMR DOCUMENTFEED

Notifica a una aplicación cuando el IME seleccionado necesita la cadena convertida de la aplicación. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ REQUEST**](wm-ime-request.md) con parámetros establecidos como se muestra a continuación.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a un búfer para contener la [**estructura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la estructura de cadena de reconversión actual. Si *lParam se* establece en **NULL,** la aplicación devuelve el tamaño necesario para que el búfer mantenga la estructura. El comando devuelve 0 si no se realiza correctamente.

## <a name="remarks"></a>Observaciones

El IME almacena en caché las cadenas convertida para una mayor precisión de conversión. Una limitación del almacenamiento en caché del IME es que pierde la cadena convertida en las siguientes circunstancias:

-   La posición del cursor de la aplicación se mueve mediante una clave, por ejemplo, una clave de cursor.
-   El mouse mueve la posición del cursor de la aplicación.
-   Se abre un nuevo documento.

Con el **comando \_ DOCUMENTFEED de IMR,** el IME puede actualizar sus cadenas almacenadas en caché en cualquier momento. El uso de este comando mejora la precisión de la conversión.

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

 

 




