---
description: Especifica el almacenamiento en caché de un identificador para una impresora abierta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS enumeración (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091805"
---
# <a name="printer_option_flags-enumeration"></a>ENUMERACIÓN PRINTER \_ OPTION \_ FLAGS

Especifica el almacenamiento en caché de un identificador para una impresora abierta con [**OpenPrinter2.**](openprinter2.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**OPCIÓN DE \_ IMPRESORA \_ SIN \_ CACHÉ**
</dt> <dd>

El identificador no se almacena en caché. Todas las funciones aplicadas a un identificador devuelto [**por OpenPrinter2**](openprinter2.md) irán al equipo remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**CACHÉ DE \_ OPCIONES DE \_ IMPRESORA**
</dt> <dd>

El identificador se almacena en caché. Todas las funciones aplicadas a un identificador devuelto [**por OpenPrinter2**](openprinter2.md) irán a la caché local.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**CAMBIO DE \_ CLIENTE DE OPCIÓN DE \_ \_ IMPRESORA**
</dt> <dd>

[**SetPrinter**](setprinter.md) puede usar el identificador devuelto por [**OpenPrinter2**](openprinter2.md) para cambiar el nombre de la conexión de impresora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




