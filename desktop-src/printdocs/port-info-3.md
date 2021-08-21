---
description: La estructura \_ PORT INFO \_ 3 especifica el valor de estado de un puerto de impresora.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: PORT_INFO_3 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cdd7f2fd931c7f503d566cdfc4ab38c5f595b51cea23d0cdf2fb326811cf7748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033973"
---
# <a name="port_info_3-structure"></a>Estructura \_ PORT INFO \_ 3

La **estructura PORT INFO \_ \_ 3** especifica el valor de estado de un puerto de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwStatus**
</dt> <dd>

Nuevo valor de estado del puerto. Este valor solo se usa si el **miembro pszStatus** es **NULL.**

Este miembro puede ser uno de los siguientes valores.



| Valor                            | Significado                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Borra el estado del puerto de la impresora.                     |
| ESTADO DEL \_ PUERTO \_ SIN CONEXIÓN            | La impresora del puerto está sin conexión.                      |
| AT JAM \_ DE PAPEL DE ESTADO DEL \_ \_ PUERTO         | La impresora del puerto tiene un atraso de papel.                 |
| SALIDA DEL \_ DOCUMENTO DE ESTADO DEL \_ \_ PUERTO         | La impresora del puerto está sin papel.                 |
| UBICACIÓN DE \_ SALIDA DE ESTADO DE PUERTO \_ \_ \_ COMPLETA  | El cubo de salida de la impresora del puerto está lleno.            |
| PROBLEMA DE \_ PAPEL DE ESTADO DEL \_ \_ PUERTO     | La impresora del puerto tiene un problema de papel.             |
| ESTADO \_ DEL PUERTO SIN \_ \_ TONER          | La impresora del puerto está fuera del toner.                 |
| PUERTA \_ DE ESTADO DEL PUERTO \_ \_ ABIERTA         | La puerta de la impresora del puerto está abierta.             |
| INTERVENCIÓN \_ DEL USUARIO DEL ESTADO DEL \_ \_ PUERTO | La impresora del puerto requiere la intervención del usuario.      |
| ESTADO \_ DEL PUERTO FUERA DE \_ \_ \_ MEMORIA    | La impresora del puerto está sin memoria.                |
| PUERTO \_ DE ESTADO DE \_ TONER \_ BAJO         | La impresora del puerto tiene poca toner.                 |
| ESTADO \_ DEL PUERTO EN \_ \_ CALIENTE        | La impresora del puerto está en proceso de configuración.                   |
| ESTADO DEL \_ PUERTO \_ POWER \_ SAVE        | La impresora del puerto está en modo de alimentación. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Puntero a una nueva cadena de valor de estado de puerto de impresora que se establecerá. Use este miembro si no hay ningún valor de estado adecuado entre los enumerados para **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

Gravedad del valor de estado del puerto.

Este miembro puede ser uno de los siguientes valores.



| Valor                       | Significado                                   |
|-----------------------------|-------------------------------------------|
| ERROR DE \_ TIPO DE ESTADO DE \_ \_ PUERTO   | El valor de estado del puerto indica un error. |
| ADVERTENCIA DE \_ TIPO DE ESTADO DE \_ \_ PUERTO | El valor de estado del puerto es una advertencia.       |
| INFORMACIÓN DE \_ TIPO DE ESTADO DE \_ \_ PUERTO    | El valor de estado del puerto es informativo.   |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad PORT STATUS TYPE ERROR, el colador de impresión deja de enviar \_ \_ trabajos al \_ puerto. El colador de impresión no reanuda el envío de trabajos al puerto hasta que se realiza otra llamada [**a SetPort**](setport.md) para borrar el estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PORT \_ INFO \_ 3W** (Unicode) e **\_ PORT INFO \_ \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




