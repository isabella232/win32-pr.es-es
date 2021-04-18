---
description: La estructura de información de la impresora \_ \_ 1 especifica información general de la impresora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Estructura de PRINTER_INFO_1 (winspool. h)
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
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720590"
---
# <a name="printer_info_1-structure"></a>Estructura de la información de la impresora \_ \_ 1

La estructura de información de la **impresora \_ \_ 1** especifica información general de la impresora.

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

Especifica información sobre los datos devueltos. A continuación se muestran los valores de este miembro.



| Value                    | Significado                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_expansión de enum de impresora \_    | Un proveedor de impresión puede establecer esta marca como una sugerencia para una aplicación que llama para enumerar este objeto más allá si está habilitada la expansión predeterminada. Por ejemplo, cuando se enumeran los dominios, un proveedor de impresión puede indicar el dominio del usuario mediante el establecimiento de esta marca. |
| \_contenedor de enum de impresora \_ | Si se establece esta marca, el objeto de impresora puede contener objetos enumerables. Por ejemplo, el objeto puede ser un servidor de impresión que contiene impresoras.                                                                                                             |
| \_Enumeración de impresora \_ ICON1     | Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un nombre de red de nivel superior, como la red de Microsoft Windows.                                                                                           |
| \_Enumeración de impresora \_ ICON2     | Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un dominio de red.                                                                                                                                  |
| \_Enumeración de impresora \_ ICON3     | Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un servidor de impresión.                                                                                                                                    |
| \_Enumeración de impresora \_ ICON4     | Reservado.                                                                                                                                                                                                                                                 |
| \_Enumeración de impresora \_ ICON5     | Reservado.                                                                                                                                                                                                                                                 |
| \_Enumeración de impresora \_ ICON6     | Reservado.                                                                                                                                                                                                                                                 |
| \_Enumeración de impresora \_ ICON7     | Reservado.                                                                                                                                                                                                                                                 |
| \_Enumeración de impresora \_ ICON8     | Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como una impresora.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Puntero a una cadena terminada en null que describe el contenido de la estructura.

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que nombra el contenido de la estructura.

</dd> <dt>

**pComment**
</dt> <dd>

Puntero a una cadena terminada en null que contiene datos adicionales que describen la estructura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 1W** (Unicode) e información de la **\_ impresora \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




