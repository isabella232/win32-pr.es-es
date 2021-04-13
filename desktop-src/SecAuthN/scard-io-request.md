---
description: La estructura de \_ solicitud de e/s PPAC \_ comienza una estructura de información de control de protocolo.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: SCARD_IO_REQUEST estructura (Winsmcrd. h)
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
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360663"
---
# <a name="scard_io_request-structure"></a>Estructura de \_ solicitud de e/s de PPAC \_

La estructura de **\_ \_ solicitud de e/s PPAC** comienza una estructura de información de control de protocolo. Cualquier información específica del protocolo sigue inmediatamente a esta estructura. La longitud completa de la estructura debe estar alineada con el tamaño de la palabra de la arquitectura de hardware subyacente. Por ejemplo, en Win32 la longitud de cualquier información de PCI debe ser un múltiplo de cuatro bytes para que se alinee en un límite de 32 bits.

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

Longitud, en bytes, de la estructura de **\_ \_ solicitud de e/s** integrada más cualquier información específica de PCI siguiente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Winsmcrd. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




