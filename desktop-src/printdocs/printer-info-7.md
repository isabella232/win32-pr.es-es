---
description: La estructura PRINTER \_ INFO \_ 7 especifica la información de impresora de servicios de directorio.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: PRINTER_INFO_7 estructura (Winspool.h)
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
ms.openlocfilehash: c8ba37176bb970883533be1e0ddcc47a09b164bf48767442f75096828c9bce5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867771"
---
# <a name="printer_info_7-structure"></a>Estructura PRINTER \_ INFO \_ 7

La **estructura PRINTER INFO \_ \_ 7** especifica la información de impresora de servicios de directorio. Use esta estructura con la función [**SetPrinter**](setprinter.md) para publicar los datos de una impresora en el servicio de directorio (DS) o para actualizar o quitar los datos publicados de una impresora del DS. Use esta estructura con la [**función GetPrinter**](getprinter.md) para determinar si una impresora está publicada en el DS.

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

Puntero a una cadena terminada en NULL que contiene el GUID del objeto de cola de impresión del servicio de directorio asociado a una impresora publicada. Use la [**función GetPrinter**](getprinter.md) para recuperar este GUID.

Antes de [**llamar a SetPrinter,**](setprinter.md)establezca **pszObjectGUID** en **NULL.**

</dd> <dt>

**dwAction**
</dt> <dd>

Indica la acción que debe realizar [**la función SetPrinter.**](setprinter.md) Para la [**función GetPrinter,**](getprinter.md) este miembro indica si se publica la impresora especificada. Este miembro puede ser una combinación de los valores siguientes.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_ Pending**</dt> <dt>0x80000000</dt> </dl>       | [**GetPrinter:**](getprinter.md)indica que el sistema está intentando completar una operación de publicación o despublicación iniciada por una [**llamada a SetPrinter.**](setprinter.md)<br/> [**SetPrinter:**](setprinter.md)este valor no es válido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ Publicar**</dt> <dt>0x00000001</dt> </dl>       | [**SetPrinter:**](setprinter.md)publica los datos de la impresora en el DS.<br/> [**GetPrinter:**](getprinter.md)indica que la impresora está publicada. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ Volver a publicar**</dt> <dt>0x00000008</dt> </dl> | [**SetPrinter:**](setprinter.md)los datos de DS de la impresora no se publican y, a continuación, se publican de nuevo, actualizando todas las propiedades de la impresora publicada. Volver a publicar también cambia el GUID de la impresora publicada.<br/> [**GetPrinter:**](getprinter.md)nunca devuelve este valor. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Anular la publicación**</dt> <dt>0x00000004</dt> </dl> | [**SetPrinter:**](setprinter.md)quita los datos publicados de la impresora del DS.<br/> [**GetPrinter:**](getprinter.md)indica que la impresora no está publicada. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ ACTUALIZAR**</dt> <dt>0x00000002</dt> </dl>          | [**SetPrinter:**](setprinter.md)actualiza los datos publicados de la impresora en el DS.<br/> [**GetPrinter:**](getprinter.md)nunca devuelve este valor. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **estructura PRINTER INFO \_ \_ 7** se usa en una llamada a [**SetPrinter**](setprinter.md) para publicar información de impresora en el servicio de directorio. Los datos publicados incluyen todos los valores y datos de la impresora especificada que se encuentran en las claves SPLDS \_ SPOOLER KEY, SPLDS DRIVER KEY o SPLDS USER KEY creadas por \_ \_ \_ \_ \_ [**SetPrinterDataEx**](setprinterdataex.md).

Para [**SetPrinter,**](setprinter.md) *pszObjectGUID* debe establecerse en **NULL.** Para [**GetPrinter,**](getprinter.md) *pszObjectGUID* devuelve el GUID del objeto de cola de impresión de servicios de directorio asociado a una impresora publicada. Puede usar este GUID con métodos Active Directory Services Interface (ADSI) para recuperar los datos publicados de la impresora. Sin embargo, el método recomendado para recuperar datos publicados es llamar a la [**función GetPrinterDataEx.**](getprinterdataex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 7W** (Unicode) e **\_ PRINTER INFO \_ \_ 7A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




