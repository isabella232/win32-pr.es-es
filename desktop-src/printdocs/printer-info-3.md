---
description: La estructura PRINTER \_ INFO \_ 3 especifica la información de seguridad de la impresora.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: PRINTER_INFO_3 estructura (Winspool.h)
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
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867930"
---
# <a name="printer_info_3-structure"></a>Estructura PRINTER \_ INFO \_ 3

La **estructura PRINTER INFO \_ \_ 3** especifica la información de seguridad de la impresora.

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

Puntero a una [**estructura \_ DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que especifica la información de seguridad de una impresora.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura PRINTER INFO \_ \_ 3** permite a una aplicación obtener y establecer el descriptor de seguridad de una impresora. El autor de la llamada puede hacerlo incluso si carece de permisos de impresora específicos, siempre que tenga los derechos estándar descritos en [**SetPrinter**](setprinter.md) y [**GetPrinter**](getprinter.md). Por lo tanto, una aplicación puede denegar temporalmente todo el acceso a una impresora, al tiempo que permite que el propietario de la impresora tenga acceso a la ACL discrecional de la impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**DESCRIPTOR \_ DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

