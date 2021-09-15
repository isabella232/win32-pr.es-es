---
title: WM_DDE_POKE mensaje (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje \_ WM DDE \_ WM DHCPE a una aplicación de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE mensaje Datos Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570012"
---
# <a name="wm_dde_poke-message"></a>Mensaje \_ DE WM DDE DE VEZ EN \_ DÍA

Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje **\_ WM DDE \_ TFTPE** a una aplicación de servidor DDE. Un cliente usa este mensaje para solicitar al servidor que acepte un elemento de datos no solicitado. Se espera que el servidor responda con un mensaje [**\_ wm DDE \_ ACK**](wm-dde-ack.md) que indica si aceptó el elemento de datos.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


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

La palabra de orden bajo es un identificador de un objeto de memoria global que contiene una estructura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) con los datos y la información adicional.

La palabra de orden superior contiene un atom global que identifica el elemento de datos para el que se envían los datos o la notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Publicar

La aplicación cliente debe asignar memoria para el objeto de memoria global mediante la [**función GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) La aplicación cliente debe eliminar el objeto si se cumple alguna de las condiciones siguientes:

-   La aplicación de servidor responde con un mensaje [**WM \_ DDE \_ ACK**](wm-dde-ack.md) negativo.
-   El **miembro fRelease** es **FALSE,** pero la aplicación de servidor responde con un [**DDE ACK de WM \_ positivo o \_ negativo.**](wm-dde-ack.md)

La aplicación cliente debe crear el atom mediante la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

La aplicación cliente debe crear o volver a usar el parámetro **\_ WM DDE \_ MQE** *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

### <a name="receiving"></a>Recepción

La aplicación de servidor debe publicar el [**mensaje \_ wm DDE \_ ACK**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **WM \_ DDE \_ ACK,** el servidor puede reutilizar el atom o puede eliminarlo y crear uno nuevo.

El servidor debe crear o reutilizar el parámetro [**wm \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Para liberar el objeto de memoria global, el servidor debe llamar a la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree) Además, si el formato de datos es [**\_ CF DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT,** el servidor también debe llamar a [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con el identificador de metarchivo incrustado. Estos dos formatos tienen un nivel adicional de direccionamiento indirecto; Es decir, una aplicación debe bloquear el objeto para obtener un puntero a un identificador, bloquear ese identificador para obtener un puntero a una estructura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) y, por último, llamar a **DeleteMetaFile** con el identificador del **miembro hMF** de la estructura **METAFILEPICT.**

Para liberar el objeto , el servidor debe llamar a [**la función FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



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

[**DesempaquetarDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

