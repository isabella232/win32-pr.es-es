---
description: La estructura SCARD \_ IO REQUEST comienza una estructura de información de control de \_ protocolo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST estructura (Winsmcrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: 9a377643e794b679be593bb99b8750698c92dd3aa8abacd79bfdb1c478c9c7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918900"
---
# <a name="scard_io_request-structure"></a>Estructura SCARD \_ IO \_ REQUEST

La **estructura SCARD \_ IO REQUEST \_ comienza** una estructura de información de control de protocolo. Cualquier información específica del protocolo sigue inmediatamente a esta estructura. Toda la longitud de la estructura debe alinearse con el tamaño de palabra de la arquitectura de hardware subyacente. Por ejemplo, en Win32, la longitud de cualquier información de PCI debe ser un múltiplo de cuatro bytes para que se alinee en un límite de 32 bits.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwProtocol**
</dt> <dd>

Protocolo en uso.

</dd> <dt>

**cbPciLength**
</dt> <dd>

Longitud, en bytes, de la estructura **SCARD \_ IO \_ REQUEST** más cualquier siguiente información específica de PCI.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winsmcrd.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




