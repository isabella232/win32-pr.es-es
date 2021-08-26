---
description: La estructura PRINTER \_ NOTIFY INFO contiene información de impresora devuelta por la función \_ FindNextPrinterChangeNotification. La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO estructura (Winspool.h)
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
ms.openlocfilehash: 26c7fca07eda8638bf657055691d72c78bccdbec6ef2b9a8c76ee7cf830bc767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091855"
---
# <a name="printer_notify_info-structure"></a>PRINTER \_ NOTIFY \_ INFO (estructura)

La **estructura PRINTER NOTIFY \_ \_ INFO** contiene información de impresora devuelta por [**la función FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md) La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.

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

Marca de bits que indica el estado de la estructura de notificación. Si el bit PRINTER NOTIFY INFO DISCARDED está establecido, indica que se han tenido que \_ \_ descartar algunas \_ notificaciones.

</dd> <dt>

**Recuento**
</dt> <dd>

Número de elementos [**PRINTER \_ NOTIFY INFO \_ \_ DATA**](printer-notify-info-data.md) de la **matriz aData.**

</dd> <dt>

**Adata**
</dt> <dd>

Matriz de estructuras [**DE DATOS DE PRINTER NOTIFY \_ \_ INFO. \_**](printer-notify-info-data.md) Cada elemento de la matriz identifica un único campo de información de trabajo o impresora y proporciona los datos actuales para ese campo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el **miembro Flags** tiene el conjunto de bits PRINTER \_ NOTIFY INFO \_ DISCARDED, esto indica que se ha producido un desbordamiento o un error, y es posible que se hayan perdido \_ las notificaciones. En este caso, debe llamar a [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) y especificar la marca PRINTER \_ NOTIFY OPTIONS REFRESH para recuperar toda la información \_ \_ actual. Hasta que solicite esta operación de actualización, el sistema no enviará notificaciones adicionales para este objeto de notificación de cambio.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**DATOS DE \_ INFORMACIÓN DE NOTIFICACIÓN DE \_ \_ IMPRESORA**](printer-notify-info-data.md)
</dt> </dl>

 

 




