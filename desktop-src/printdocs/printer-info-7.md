---
description: La estructura de la información de la impresora \_ \_ 7 especifica la información de la impresora de servicios de directorio.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Estructura de PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716943"
---
# <a name="printer_info_7-structure"></a>Estructura de información de impresora \_ \_ 7

La estructura de la información de la **impresora \_ \_ 7** especifica la información de la impresora de servicios de directorio. Utilice esta estructura con la función [**SetPrinter**](setprinter.md) para publicar los datos de una impresora en el servicio de directorio (DS), o para actualizar o quitar los datos publicados de la impresora del DS. Use esta estructura con la función [**GetPrinter**](getprinter.md) para determinar si una impresora está publicada en el DS.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Puntero a una cadena terminada en null que contiene el GUID del objeto de cola de impresión del servicio de directorio asociado a una impresora publicada. Utilice la función [**GetPrinter**](getprinter.md) para recuperar este GUID.

Antes de llamar a [**SetPrinter**](setprinter.md), establezca **pszObjectGUID** en **null**.

</dd> <dt>

**dwAction**
</dt> <dd>

Indica la acción que va a realizar la función [**SetPrinter**](setprinter.md) . En el caso de la función [**GetPrinter**](getprinter.md) , este miembro indica si la impresora especificada está publicada. Este miembro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ FUNCIÓN**</dt> <dt>0x80000000</dt> pendiente </dl>       | [**GetPrinter**](getprinter.md): indica que el sistema está intentando completar una operación de publicación o anulación de publicación iniciada por una llamada a [**SetPrinter**](setprinter.md) .<br/> [**SetPrinter**](setprinter.md): este valor no es válido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBLICAR**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter**](setprinter.md): publica los datos de la impresora en el DS.<br/> [**GetPrinter**](getprinter.md): indica que la impresora está publicada. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ VOLVER a publicar**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter**](setprinter.md): los datos de DS de la impresora no se publican y, a continuación, se vuelven a publicar, actualizando todas las propiedades de la impresora publicada. Al volver a publicar también se cambia el GUID de la impresora publicada.<br/> [**GetPrinter**](getprinter.md): nunca devuelve este valor. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Cancelar la publicación**</dt> de <dt>0x00000004</dt> </dl> | [**SetPrinter**](setprinter.md): quita los datos publicados de la impresora del DS.<br/> [**GetPrinter**](getprinter.md): indica que la impresora no está publicada. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ ACTUALIZAR**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter**](setprinter.md): actualiza los datos publicados de la impresora en el DS.<br/> [**GetPrinter**](getprinter.md): nunca devuelve este valor. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de la información de la **impresora \_ \_ 7** se usa en una llamada a [**SetPrinter**](setprinter.md) para publicar información de impresora en el servicio de directorio. Los datos publicados incluyen todos los valores y datos de la impresora especificada que se encuentra en la clave de administrador de trabajos de SPLDS \_ \_ , \_ clave de controlador SPLDS \_ o claves de clave de usuario de SPLDS \_ \_ creadas por [**SetPrinterDataEx**](setprinterdataex.md).

En el caso de [**SetPrinter**](setprinter.md), *pszObjectGUID* debe establecerse en **null**. Para [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* devuelve el GUID del objeto cola de impresión de servicios de directorio asociado a una impresora publicada. Puede usar este GUID con métodos de la interfaz de Active Directory Services (ADSI) para recuperar los datos publicados para la impresora. Sin embargo, el método recomendado para recuperar los datos publicados es llamar a la función [**GetPrinterDataEx**](getprinterdataex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 7W** (Unicode) y la información de la **\_ impresora \_ \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




