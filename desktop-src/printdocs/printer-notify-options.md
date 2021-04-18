---
description: La estructura de opciones de notificación de impresora \_ \_ especifica opciones para un objeto de notificación de cambios que supervisa una impresora o un servidor de impresión.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Estructura de PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720574"
---
# <a name="printer_notify_options-structure"></a>Estructura de opciones de \_ notificación de impresora \_

La estructura de **\_ \_ Opciones** de notificación de impresora especifica opciones para un objeto de notificación de cambios que supervisa una impresora o un servidor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. Establezca este miembro en 2.

</dd> <dt>

**Marcas**
</dt> <dd>

Marca de bits. Si establece la marca de \_ \_ actualización de opciones \_ de notificación de impresora en una llamada a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la función proporciona los datos actuales de todos los campos supervisados de información de la impresora. La función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) omite el miembro **Flags** .

</dd> <dt>

**Recuento**
</dt> <dd>

Número de elementos de la matriz **pTypes** .

</dd> <dt>

**pTypes**
</dt> <dd>

Puntero a una matriz de estructuras [**de \_ \_ \_ tipo de opciones de notificación de impresora**](printer-notify-options-type.md) . Utilice un elemento de esta matriz para especificar los campos de información de la impresora que se van a supervisar y un elemento para especificar los campos de información de los trabajos que se van a supervisar. Puede supervisar la información de la impresora, la información del trabajo o ambas cosas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use esta estructura con la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar el conjunto de campos de información de la impresora o del trabajo para supervisar los cambios.

Use esta estructura con la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar los datos actuales de todos los campos supervisados de información de la impresora y del trabajo. En este caso, el miembro **Flags** especifica la \_ marca de actualización opciones de notificación de impresora \_ \_ y la función omite los demás miembros de la estructura.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_tipo de \_ Opciones de notificación de impresora \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




