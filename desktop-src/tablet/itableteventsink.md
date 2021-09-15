---
description: Define métodos que controlan los eventos de la interfaz ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: ITabletEventSink (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467975"
---
# <a name="itableteventsink-interface"></a>ITabletEventSink (interfaz)

Define métodos que controlan los [**eventos de la interfaz ITablet.**](itablet.md)

## <a name="members"></a>Members

La **interfaz ITabletEventSink** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletEventSink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITabletEventSink** tiene estos métodos.



| Método                                                        | Descripción                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Se produce cuando se crea un nuevo contexto de tableta.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Se produce cuando se destruye un contexto de tableta.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Se produce cuando la punta del lápiz se pone en contacto con la superficie de digitalización de la tableta.<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | Se produce cuando un lápiz óptico se encuentra dentro del intervalo de detección del digitalizador.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Se produce cuando el cursor se mueve sobre el digitalizador de tabletas.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Se produce cuando se agrega un nuevo lápiz óptico al sistema.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Se produce cuando el lápiz óptico sale del intervalo de detección físico (proximidad) de la tableta.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Se produce cuando el usuario ha elevado el lápiz óptico de la superficie del digitalizador de tabletas.<br/>         |
| [**Paquetes**](itableteventsink-packets.md)                   | Se produce cuando el lápiz óptico se mueve en el digitalizador.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Se produce cuando hay disponible un evento del sistema.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

Los desarrolladores no deben usar esta interfaz.

El código siguiente muestra cómo se define la interfaz **ITabletEventSink.**

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

