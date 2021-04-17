---
description: La \_ estructura PRINTPROCESSOR caps \_ 1 es el formato de la información de funcionalidad de la impresora que devuelve la función GetPrinterData en el búfer especificado por la variable pdata.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Estructura de PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697512"
---
# <a name="printprocessor_caps_1-structure"></a>\_Estructura PRINTPROCESSOR Cap \_ 1

La estructura **PRINTPROCESSOR \_ caps \_ 1** es el formato de la información de funcionalidad de la impresora que devuelve la función [**GetPrinterData**](getprinterdata.md) en el búfer especificado por la variable *pdata* .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwLevel**
</dt> <dd>

Número de versión de la estructura. Este valor debe ser 1.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Máscara de bits que representa los diversos números de páginas del documento que la impresora puede imprimir en una página física. El bit menos significativo representa 1 página de documento por página, el siguiente bit representa 2 páginas de documento por página, etc. Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por página física.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

El orden en que se imprimirán las páginas. Este valor puede ser \_ impresión normal, impresión inversa \_ o folleto \_ impreso.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Número máximo de copias que la impresora puede controlar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores de todos los miembros de la estructura se proporcionan mediante la función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , que se documenta en el kit de controladores de Windows (WDK).

El administrador de trabajos de impresión llama a la función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) de un procesador de impresión cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), especificando un nombre de valor con un formato de PrintProcCaps \_ *DataType*, donde *DataType* es el nombre de un tipo de datos de entrada.

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

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

