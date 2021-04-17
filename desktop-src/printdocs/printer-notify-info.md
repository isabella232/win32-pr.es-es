---
description: La estructura de información de notificación de impresora \_ \_ contiene información de la impresora devuelta por la función FindNextPrinterChangeNotification. La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Estructura de PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687742"
---
# <a name="printer_notify_info-structure"></a>Estructura de información de \_ notificación de impresora \_

La estructura de **\_ \_ información de notificación de impresora** contiene información de la impresora devuelta por la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Versión de esta estructura. Establezca este miembro en 2.

</dd> <dt>

**Marcas**
</dt> <dd>

Marca de bits que indica el estado de la estructura de notificación. Si \_ \_ se establece el bit descartado de la información de notificación de impresora \_ , indica que se tuvieron que descartar algunas notificaciones.

</dd> <dt>

**Recuento**
</dt> <dd>

El número de elementos de datos de la información de  notificación de [**impresora \_ \_ \_**](printer-notify-info-data.md) en la matriz de Adatum.

</dd> <dt>

**Adatum**
</dt> <dd>

Una matriz de estructuras de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora. Cada elemento de la matriz identifica un solo campo de información de trabajo o de impresora y proporciona los datos actuales para ese campo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el miembro **Flags** tiene el \_ \_ conjunto de bits descartado de información de notificación de impresora \_ , esto indica que se ha producido un desbordamiento o un error, y que es posible que se hayan perdido las notificaciones. En este caso, debe llamar a [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) y especificar la \_ marca de actualización de opciones de notificación de impresora \_ \_ para recuperar toda la información actual. Hasta que solicite esta operación de actualización, el sistema no enviará notificaciones adicionales para este objeto de notificación de cambios.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_datos de \_ información de notificación de impresora \_**](printer-notify-info-data.md)
</dt> </dl>

 

 




