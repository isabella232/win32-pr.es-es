---
description: La \_ \_ \_ estructura de tipo de opciones de notificación de impresora especifica el conjunto de campos de información de la impresora o del trabajo que va a supervisar un objeto de notificación de cambio de impresora. Una llamada a la función FindFirstPrinterChangeNotification especifica una \_ \_ estructura de opciones de notificación de impresora, que contiene una matriz de \_ estructuras de tipo opciones de notificación de impresora \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Estructura de PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
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
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716253"
---
# <a name="printer_notify_options_type-structure"></a>\_Estructura de \_ tipo de opciones de notificación de impresora \_

La estructura de tipo de opciones de notificación de impresora especifica el conjunto de campos de información de la impresora o del trabajo que va a supervisar un objeto de notificación de cambio de impresora. **\_ \_ \_**

Una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) especifica una estructura de [**\_ \_ Opciones de notificación de impresora**](printer-notify-options.md) , que contiene una matriz de estructuras de **\_ \_ \_ tipo opciones de notificación de impresora** .

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

Tipo que se va a inspeccionar. Este miembro puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                      | Significado                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Trabajo \_ de NOTIFICAr \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica que los campos especificados en la matriz **pFields** son \_ constantes de campo de notificación de trabajo \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Impresora \_ de NOTIFICAr el \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica que los campos especificados en la matriz **pFields** son \_ constantes de campo de notificación de impresora \_ \_ \* .<br/> |



 

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

Número de elementos de la matriz **pFields** .

</dd> <dt>

**pFields**
</dt> <dd>

Puntero a una matriz de valores. Cada elemento de la matriz especifica un campo de información de trabajo o impresora de interés. Para obtener una lista de los campos de información de la impresora y el trabajo admitidos, consulte la estructura de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora.

</dd> </dl>

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_datos de \_ información de notificación de impresora \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opciones de notificación de impresora \_**](printer-notify-options.md)
</dt> </dl>

 

 




