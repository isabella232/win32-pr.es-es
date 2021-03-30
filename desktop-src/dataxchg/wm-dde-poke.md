---
title: Mensaje de WM_DDE_POKE (DDE. h)
description: Una aplicación cliente Intercambio dinámico de datos (DDE) envía un mensaje de mensajes de envío de WM \_ DDE \_ a una aplicación de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Intercambio de datos de mensajes de WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803920"
---
# <a name="wm_dde_poke-message"></a>\_Mensaje de mensaje de error de WM DDE \_

Una aplicación cliente Intercambio dinámico de datos (DDE) envía un mensaje de mensajes de envío de **WM \_ DDE \_** a una aplicación de servidor DDE. Un cliente usa este mensaje para solicitar al servidor que acepte un elemento de datos no solicitado. Se espera que el servidor responda con un mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) que indica si aceptó el elemento de datos.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) con los datos e información adicional.

La palabra de orden superior contiene un átomo global que identifica el elemento de datos para el que se envían los datos o la notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Config

La aplicación cliente debe asignar memoria para el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . La aplicación cliente debe eliminar el objeto si se cumple alguna de las condiciones siguientes:

-   La aplicación de servidor responde con un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) negativo.
-   El miembro **fRelease** es **false**, pero la aplicación de servidor responde con una [**confirmación de WM \_ DDE \_**](wm-dde-ack.md)positiva o negativa.

La aplicación cliente debe crear el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

La aplicación cliente debe crear o reutilizar el parámetro *lParam* de **WM \_ DDE \_** , llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

### <a name="receiving"></a>Recepción

La aplicación de servidor debe publicar el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **la \_ \_ confirmación de WM DDE**, el servidor puede volver a usar el átomo, o bien puede eliminarlo y crear uno nuevo.

El servidor debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Para liberar el objeto de memoria global, el servidor debe llamar a la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Además, si el formato de los datos es [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT**, el servidor también debe llamar a [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con el identificador de metarchivo incrustado. Estos dos formatos tienen un nivel de direccionamiento indirecto adicional. es decir, una aplicación debe bloquear el objeto para obtener un puntero a un identificador y, a continuación, bloquear ese identificador para obtener un puntero a una estructura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) y, por último, llamar a **DeleteMetaFile** con el identificador del miembro **hMF** de la estructura **METAFILEPICT** .

Para liberar el objeto, el servidor debe llamar a la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_confirmación de DDE de WM \_**](wm-dde-ack.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

