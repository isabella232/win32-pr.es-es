---
description: Define métodos que controlan los eventos de la interfaz ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interfaz ITabletEventSink
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279173"
---
# <a name="itableteventsink-interface"></a>Interfaz ITabletEventSink

Define métodos que controlan los eventos de la [**interfaz ITablet**](itablet.md) .

## <a name="members"></a>Miembros

La interfaz **ITabletEventSink** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletEventSink** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITabletEventSink** tiene estos métodos.



| Método                                                        | Descripción                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Se produce cuando se crea un nuevo contexto de Tablet PC.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Se produce cuando se destruye un contexto de Tablet PC.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Se produce cuando la punta del lápiz se pone en contacto con la superficie de la tableta de la digitalización.<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | Se produce cuando un lápiz entra dentro del intervalo de detección del digitalizador.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Se produce cuando se agrega un nuevo lápiz al sistema.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Se produce cuando el lápiz deja el intervalo de detección física (proximidad) de la tableta.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Se produce cuando el usuario ha generado el lápiz óptico desde la superficie del digitalizador de Tablet PC.<br/>         |
| [**Paquetes**](itableteventsink-packets.md)                   | Se produce cuando el lápiz óptico se mueve en el digitalizador.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Se produce cuando hay un evento del sistema disponible.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

Los desarrolladores no deben utilizar esta interfaz.

En el código siguiente se muestra cómo se define la interfaz **ITabletEventSink** .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

