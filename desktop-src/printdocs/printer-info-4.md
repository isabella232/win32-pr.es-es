---
description: La estructura de la información de la impresora \_ \_ 4 especifica información general de la impresora. La estructura se puede usar para recuperar la información mínima de la impresora en una llamada a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Estructura de PRINTER_INFO_4 (winspool. h)
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
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278196"
---
# <a name="printer_info_4-structure"></a>Estructura de la información de la impresora \_ \_ 4

La estructura de la información de la **impresora \_ \_ 4** especifica información general de la impresora.

La estructura se puede usar para recuperar la información mínima de la impresora en una llamada a [**EnumPrinters**](enumprinters.md). Esta llamada es una manera rápida y sencilla de recuperar los nombres y atributos de todas las impresoras instaladas localmente en un sistema y todas las conexiones de impresora remotas que ha establecido un usuario.

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

Puntero a una cadena terminada en null que especifica el nombre de la impresora (local o remota).

</dd> <dt>

**pServerName**
</dt> <dd>

Puntero a una cadena terminada en null que es el nombre del servidor.

</dd> <dt>

**Atributos**
</dt> <dd>

Especifica información sobre los datos devueltos.



| Value                       | Significado                          |
|-----------------------------|----------------------------------|
| atributo de impresora \_ \_ local   | La impresora es una impresora local.  |
| \_red de atributos de impresora \_ | La impresora es una impresora remota. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de la información de la **impresora \_ \_ 4** proporciona una manera fácil y sumamente rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que ha establecido un usuario. Cuando se llama a [**EnumPrinters**](enumprinters.md) con una estructura de datos de la información de la **impresora \_ \_ 4** , esa función consulta el registro para obtener la información especificada y, a continuación, vuelve inmediatamente. Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de estructuras de datos de la información de la **impresora \_ \_ XXX** . En concreto, cuando se llama a **EnumPrinters** con una estructura de datos de nivel 2 (información de la **impresora \_ \_ 2** ), realiza una llamada **OpenPrinter** en cada conexión remota. Si una conexión remota está inactiva, si el servidor remoto ya no existe, o si la impresora remota ya no existe, la función debe esperar a que se agote el tiempo de espera de RPC y, por tanto, no se puede realizar la llamada a **OpenPrinter** . Esto puede tardar unos minutos. Pasar una estructura de la información de la **impresora \_ \_ 4** permite que una aplicación recupere un mínimo de la información necesaria; si se desea obtener información más detallada, se puede realizar una llamada posterior al nivel 2 de **EnumPrinter** .

**Los atributos** también pueden contener valores que se definen en el campo **atributos** de la información de la **impresora \_ \_ 2**.

Algunas configuraciones de impresora, como las conexiones de impresora a algunos servidores de impresión no basados en Windows, pueden devolver el **atributo de impresora \_ \_ local** y la **red de \_ atributos \_ de impresora**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 4W** (Unicode) y la información de la **\_ impresora \_ \_ 4A** (ANSI)<br/>                           |



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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> </dl>

 

 




