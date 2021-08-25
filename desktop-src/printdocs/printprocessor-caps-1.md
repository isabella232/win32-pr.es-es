---
description: La estructura PRINTPROCESSOR CAPS 1 es el formato de la información de funcionalidad de impresora que devuelve la función GetPrinterData en el búfer especificado por la \_ \_ variable pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: PRINTPROCESSOR_CAPS_1 estructura (Winspool.h)
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
ms.openlocfilehash: d057914ef9a77c7a545817b205f919afa66fdd3bc154363f7e33a9a5ba43c446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824795"
---
# <a name="printprocessor_caps_1-structure"></a>PRINTPROCESSOR \_ CAPS \_ 1 (estructura)

La **estructura PRINTPROCESSOR \_ CAPS \_ 1** es el formato de la información de funcionalidad de impresora que devuelve la función [**GetPrinterData**](getprinterdata.md) en el búfer especificado por la variable *pData.*

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

Máscara de bits que representa los distintos números de páginas de documento que la impresora puede imprimir en una página física. El bit menos significativo representa 1 página de documento por página, el bit siguiente representa 2 páginas de documento por página, y así sucesivamente. Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por página física.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Orden en el que se imprimirán las páginas. Este valor puede ser NORMAL \_ PRINT, REVERSE \_ PRINT o RESALTE \_ PRINT.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Número máximo de copias que la impresora puede controlar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) proporciona valores para todos los miembros de la estructura, que se documenta en Windows Driver Kit (WDK).

El colador llama a la función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) de un procesador de impresión cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), especificando un nombre de valor con un formato de tipo de datos PrintProcCaps , donde \_  *datatype* es el nombre de un tipo de datos de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

