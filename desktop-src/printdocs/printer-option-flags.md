---
description: Especifica el almacenamiento en caché de un identificador para una impresora abierta con OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumeración PRINTER_OPTION_FLAGS (winspool. h)
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
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278344"
---
# <a name="printer_option_flags-enumeration"></a>\_Enumeración de marcas de opción de impresora \_

Especifica el almacenamiento en caché de un identificador para una impresora abierta con [**OpenPrinter2**](openprinter2.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**opción de impresora \_ \_ sin \_ caché**
</dt> <dd>

El identificador no está almacenado en caché. Todas las funciones que se aplican a un identificador devuelto por [**OpenPrinter2**](openprinter2.md) Irán al equipo remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_caché de opciones de impresora \_**
</dt> <dd>

El identificador está almacenado en caché. Todas las funciones que se aplican a un identificador devuelto por [**OpenPrinter2**](openprinter2.md) Irán a la memoria caché local.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**\_cambio de \_ cliente de opción de impresora \_**
</dt> <dd>

[**SetPrinter**](setprinter.md) puede usar el identificador devuelto por [**OpenPrinter2**](openprinter2.md) para cambiar el nombre de la conexión de impresora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




