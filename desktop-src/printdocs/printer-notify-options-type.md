---
description: La estructura PRINTER NOTIFY OPTIONS TYPE especifica el conjunto de campos de información de impresora o trabajo que va a supervisar un objeto de notificación de cambio \_ \_ de \_ impresora. Una llamada a la función FindFirstPrinterChangeNotification especifica una estructura PRINTER NOTIFY OPTIONS, que contiene una matriz de estructuras \_ \_ PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: PRINTER_NOTIFY_OPTIONS_TYPE estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2b593a502a668345cdd0206b4f1363cf160074b6c9aa26696427b5b42a0fbdc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056282"
---
# <a name="printer_notify_options_type-structure"></a>PRINTER \_ NOTIFY \_ OPTIONS \_ (ESTRUCTURA DE TIPO)

La **estructura PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE** especifica el conjunto de campos de información de impresora o trabajo que va a supervisar un objeto de notificación de cambio de impresora.

Una llamada a [**la función FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) especifica una estructura [**PRINTER NOTIFY \_ \_ OPTIONS,**](printer-notify-options.md) que contiene una matriz de estructuras **PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.**

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo que se va a observar. Este miembro puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                      | Significado                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**JOB \_ NOTIFICACIÓN \_ DE TIPO**</dt> <dt>0x01</dt> </dl>             | Indica que los campos especificados en la matriz **pFields** son constantes JOB \_ NOTIFY \_ \_ \* FIELD.<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**IMPRESORA \_ NOTIFICACIÓN \_ DE TIPO**</dt> <dt>0x00</dt> </dl> | Indica que los campos especificados en la matriz **pFields** son constantes PRINTER \_ NOTIFY \_ \_ \* FIELD.<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**Recuento**
</dt> <dd>

Número de elementos de la matriz **pFields.**

</dd> <dt>

**pFields**
</dt> <dd>

Puntero a una matriz de valores. Cada elemento de la matriz especifica un campo de información de trabajo o impresora de interés. Para obtener una lista de los campos de información de impresoras y trabajos admitidos, vea la [**estructura PRINTER NOTIFY INFO \_ \_ \_ DATA.**](printer-notify-info-data.md)

</dd> </dl>

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**DATOS DE \_ INFORMACIÓN DE NOTIFICACIÓN DE \_ \_ IMPRESORA**](printer-notify-info-data.md)
</dt> <dt>

[**OPCIONES DE \_ NOTIFICACIÓN DE \_ IMPRESORA**](printer-notify-options.md)
</dt> </dl>

 

 




