---
description: Escribe un evento completo en una sesión.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000705"
---
# <a name="etweventwritefull-function"></a>EtwEventWriteFull función)

[La función EtwEventWriteFull y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.]

Escribe un evento completo en una sesión.

## <a name="syntax"></a>Sintaxis

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*RegHandle*
</dt> <dd>

RegHandle para el proveedor.

</dd> <dt>

*EventDescriptor* 
</dt> <dd>

Descriptor de eventos del evento que se va a registrar.

</dd> <dt>

*EventProperty*
</dt> <dd>

Marca proporcionada por el usuario.

</dd> <dt>

*ActivityId*
</dt> <dd>

ID. de actividad.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

Identificador de actividad relacionado.

</dd> <dt>

*UserDataCount*
</dt> <dd>

El número de elementos de datos de usuario.

</dd> <dt>

*UserData*
</dt> <dd>

Puntero a una matriz de elementos de datos de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Código de error de Win32.

## <a name="remarks"></a>Observaciones

La función EtwEventWriteFull y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar funciones públicas en su lugar.


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Plataforma de destino** | Windows |
| **Header** | ntetw. h |

## <a name="see-also"></a>Vea también

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[EventWriteEx](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
