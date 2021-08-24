---
description: La estructura PRINTER \_ INFO \_ 4 especifica la información general de la impresora. La estructura se puede usar para recuperar información de impresora mínima en una llamada a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: PRINTER_INFO_4 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3ba6e372b495c47dd92e61e51ba6487e6d9c2c0aca924bf6ed3a092ba0816820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446995"
---
# <a name="printer_info_4-structure"></a>Printer \_ INFO \_ 4 (estructura)

La **estructura PRINTER INFO \_ \_ 4** especifica la información general de la impresora.

La estructura se puede usar para recuperar información de impresora mínima en una llamada a [**EnumPrinters**](enumprinters.md). Esta llamada es una manera rápida y sencilla de recuperar los nombres y atributos de todas las impresoras instaladas localmente en un sistema y todas las conexiones de impresora remotas que un usuario ha establecido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora (local o remota).

</dd> <dt>

**pServerName**
</dt> <dd>

Puntero a una cadena terminada en NULL que es el nombre del servidor.

</dd> <dt>

**Atributos**
</dt> <dd>

Especifica información sobre los datos devueltos.



| Value                       | Significado                          |
|-----------------------------|----------------------------------|
| ATRIBUTO \_ DE IMPRESORA \_ LOCAL   | La impresora es una impresora local.  |
| RED DE \_ ATRIBUTOS DE \_ IMPRESORA | La impresora es una impresora remota. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura PRINTER INFO \_ \_ 4** proporciona una manera fácil y muy rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que un usuario ha establecido. Cuando se llama a [**EnumPrinters**](enumprinters.md) con una estructura de datos **PRINTER INFO \_ \_ 4,** esa función consulta al Registro la información especificada y, a continuación, devuelve inmediatamente. Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de estructuras de datos **PRINTER INFO \_ \_ xxx.** En concreto, cuando se llama a **EnumPrinters** con una estructura de datos de nivel **2 (PRINTER \_ INFO \_ 2),** realiza una llamada a **OpenPrinter** en cada conexión remota. Si una conexión remota está fuera de servicio, si el servidor remoto ya no existe o si la impresora remota ya no existe, la función debe esperar a que RPC se desasoyera y, por tanto, se producirá un error en la llamada a **OpenPrinter.** Esto puede tardar unos minutos. Pasar una **estructura PRINTER \_ INFO \_ 4** permite a una aplicación recuperar un mínimo de la información necesaria; si se desea información más detallada, se puede realizar una llamada posterior **a EnumPrinter** de nivel 2.

**Los** atributos también pueden contener valores definidos en el **campo Atributos** de PRINTER **INFO \_ \_ 2**.

Algunas configuraciones de impresora, como las conexiones de impresora a algunos servidores de impresión no basados en Windows, pueden devolver **tanto PRINTER \_ ATTRIBUTE \_ LOCAL** como **PRINTER ATTRIBUTE \_ \_ NETWORK**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 4W** (Unicode) e **\_ PRINTER INFO \_ \_ 4A** (ANSI)<br/>                           |



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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




