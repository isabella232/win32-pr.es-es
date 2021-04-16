---
description: La \_ \_ estructura de la información de puerto 3 especifica el valor de estado de un puerto de impresora.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Estructura de PORT_INFO_3 (winspool. h)
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
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706301"
---
# <a name="port_info_3-structure"></a>Estructura de la información de puerto \_ \_ 3

La estructura de la **información de puerto \_ \_ 3** especifica el valor de estado de un puerto de impresora.

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

Nuevo valor de estado del puerto. Este valor se usa solo si el miembro **pszStatus** es **null**.

Este miembro puede ser uno de los valores siguientes.



| Value                            | Significado                                             |
|----------------------------------|-----------------------------------------------------|
| 0                                | Borra el estado del puerto de impresora.                     |
| Estado de puerto \_ \_ sin conexión            | La impresora del puerto está sin conexión.                      |
| \_atasco de \_ papel de estado de puerto \_         | La impresora del puerto tiene un atasco de papel.                 |
| \_papel del estado del puerto \_ \_         | La impresora del puerto no tiene papel.                 |
| bandeja de salida de estado de puerto \_ \_ \_ \_ llena  | La bandeja de salida de printer's del puerto está llena.            |
| \_problema de \_ papel de estado de puerto \_     | La impresora del puerto tiene un problema de papel.             |
| Estado de puerto \_ \_ sin \_ tóner          | La impresora del puerto no tiene tóner.                 |
| Estado de puerto \_ \_ puerta \_ abierta         | La puerta de la impresora del puerto está abierta.             |
| Estado del puerto de \_ \_ intervención del usuario \_ | La impresora del puerto requiere la intervención del usuario.      |
| \_estado \_ de puerto \_ de \_ memoria insuficiente    | La impresora del puerto no tiene memoria suficiente.                |
| tóner de estado de puerto \_ \_ \_ bajo         | La impresora del puerto tiene poco tóner.                 |
| \_preparación del \_ estado \_ de los puertos        | La impresora del puerto se está preparando.                   |
| \_ahorro de \_ energía de estado de puerto \_        | La impresora del puerto está en modo de ahorro de energía. |



 

</dd> <dt>

**pszStatus**
</dt> <dd>

Puntero a una nueva cadena de valor de estado del puerto de impresora que se va a establecer. Utilice este miembro si no hay ningún valor de estado adecuado entre los enumerados para **dwStatus**.

</dd> <dt>

**dwSeverity**
</dt> <dd>

La gravedad del valor de estado del puerto.

Este miembro puede ser uno de los valores siguientes.



| Value                       | Significado                                   |
|-----------------------------|-------------------------------------------|
| \_error de \_ tipo de estado de puerto \_   | El valor de estado del puerto indica un error. |
| \_Advertencia de \_ tipo de estado de puerto \_ | El valor de estado del puerto es una advertencia.       |
| \_información de \_ tipo de estado de puerto \_    | El valor del estado del puerto es informativo.   |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad puerto de \_ \_ tipo \_ error, el administrador de trabajos de impresión deja de enviar trabajos al puerto. El administrador de trabajos de impresión no reanuda el envío de trabajos al puerto hasta que se realice otra llamada a [**SetPort**](setport.md) para borrar el estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Info. de **\_ Puerto \_ \_ 3W** (Unicode) y la **\_ información de puerto \_ \_ 3A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




