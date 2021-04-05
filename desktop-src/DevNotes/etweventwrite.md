---
description: 'Más información acerca de: EtwEventWrite (función)'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080244"
---
# <a name="etweventwrite-function"></a>EtwEventWrite función)

[La función EtwEventWrite y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.]

Escribe un evento básico en una sesión.

## <a name="syntax"></a>Sintaxis

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
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

*UserDataCount*
</dt> <dd>

Número de elementos de datos de usuario.

</dd> <dt>

*UserData*
</dt> <dd>

Puntero a una matriz de elementos de datos de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Código de error de Win32.


## <a name="remarks"></a>Observaciones

La función EtwEventWrite y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar funciones públicas en su lugar.

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
