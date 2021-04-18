---
description: La estructura de la información de la impresora \_ \_ 3 especifica información de seguridad de la impresora.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Estructura de PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720654"
---
# <a name="printer_info_3-structure"></a>Estructura de la información de la impresora \_ \_ 3

La estructura de la información de la **impresora \_ \_ 3** especifica información de seguridad de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntero a una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que especifica la información de seguridad de una impresora.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de la información de la **impresora \_ \_ 3** permite a una aplicación obtener y establecer el descriptor de seguridad de una impresora. El autor de la llamada puede hacerlo incluso si carece de permisos de impresora específicos, siempre y cuando tenga los derechos estándar descritos en [**SetPrinter**](setprinter.md) y [**GetPrinter**](getprinter.md). Por lo tanto, una aplicación puede denegar temporalmente el acceso a una impresora, a la vez que permite que el propietario de la impresora tenga acceso a la ACL discrecional de la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**descriptor de seguridad \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

