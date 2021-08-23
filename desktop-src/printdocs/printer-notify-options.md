---
description: La estructura OPCIONES \_ DE NOTIFICACIÓN DE IMPRESORA especifica opciones para un objeto de notificación de cambios que supervisa una impresora o \_ un servidor de impresión.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS estructura (Winspool.h)
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
ms.openlocfilehash: 57b95717e7873f0b73b66d450849d92a2c2ed7053d6d387286cc58144c772ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731137"
---
# <a name="printer_notify_options-structure"></a>PRINTER \_ NOTIFY \_ OPTIONS (estructura)

La **estructura OPCIONES DE NOTIFICACIÓN \_ \_ DE** IMPRESORA especifica opciones para un objeto de notificación de cambios que supervisa una impresora o un servidor de impresión.

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

Marca de bits. Si establece la marca PRINTER NOTIFY OPTIONS REFRESH en una llamada a la función \_ \_ \_ [**FindNextPrinterChangeNotification,**](findnextprinterchangenotification.md) la función proporciona datos actuales para todos los campos de información de impresora supervisados. La [**función FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) omite el **miembro Flags.**

</dd> <dt>

**Recuento**
</dt> <dd>

Número de elementos de la matriz **pTypes.**

</dd> <dt>

**pTypes**
</dt> <dd>

Puntero a una matriz de [**estructuras PRINTER NOTIFY OPTIONS \_ \_ \_ TYPE.**](printer-notify-options-type.md) Use un elemento de esta matriz para especificar los campos de información de impresora que se supervisarán y un elemento para especificar los campos de información de trabajo que se supervisarán. Puede supervisar la información de impresora, la información del trabajo o ambos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use esta estructura con la [**función FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar el conjunto de campos de información de impresora o trabajo para supervisar el cambio.

Use esta estructura con la [**función FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar los datos actuales de todos los campos de información de trabajo e impresora supervisados. En este caso, el **miembro Flags** especifica la marca PRINTER NOTIFY OPTIONS REFRESH y la función \_ omite los demás miembros de la \_ \_ estructura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**TIPO DE \_ OPCIONES DE NOTIFICACIÓN DE \_ \_ IMPRESORA**](printer-notify-options-type.md)
</dt> </dl>

 

 




