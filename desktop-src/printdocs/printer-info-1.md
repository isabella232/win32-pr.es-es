---
description: La estructura PRINTER \_ INFO \_ 1 especifica la información general de la impresora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ab70662371ef4ebe80b1d10f7f61700c97e979959c337bb5e81b3bc688e8c36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234212"
---
# <a name="printer_info_1-structure"></a>Printer \_ INFO \_ 1 (estructura)

La **estructura PRINTER INFO \_ \_ 1** especifica la información general de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Marcas**
</dt> <dd>

Especifica información sobre los datos devueltos. A continuación se encuentran los valores de este miembro.



| Valor                    | Significado                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EXPANSIÓN \_ DE ENUMERACIÓN \_ DE IMPRESORA    | Un proveedor de impresión puede establecer esta marca como una sugerencia para una aplicación que realiza la llamada para enumerar aún más este objeto si está habilitada la expansión predeterminada. Por ejemplo, cuando se enumeran los dominios, un proveedor de impresión podría indicar el dominio del usuario estableciendo esta marca. |
| CONTENEDOR \_ DE ENUMERACIÓN DE \_ IMPRESORA | Si se establece esta marca, el objeto de impresora puede contener objetos enumerables. Por ejemplo, el objeto puede ser un servidor de impresión que contiene impresoras.                                                                                                             |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA1     | Indica que, si procede, una aplicación debe mostrar un icono que identifique el objeto como un nombre de red de nivel superior, como Microsoft Windows Network.                                                                                           |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA2     | Indica que, si procede, una aplicación debe mostrar un icono que identifique el objeto como un dominio de red.                                                                                                                                  |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA3     | Indica que, si procede, una aplicación debe mostrar un icono que identifica el objeto como un servidor de impresión.                                                                                                                                    |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA4     | Reservado.                                                                                                                                                                                                                                                 |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA5     | Reservado.                                                                                                                                                                                                                                                 |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA6     | Reservado.                                                                                                                                                                                                                                                 |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA7     | Reservado.                                                                                                                                                                                                                                                 |
| ICONO \_ DE ENUMERACIÓN \_ DE IMPRESORA8     | Indica que, si procede, una aplicación debe mostrar un icono que identifique el objeto como una impresora.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Puntero a una cadena terminada en NULL que describe el contenido de la estructura .

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que denomina el contenido de la estructura .

</dd> <dt>

**pComment**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene datos adicionales que describen la estructura .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 1W** (Unicode) e **\_ PRINTER INFO \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




