---
description: La estructura de la información de puerto \_ \_ 2 identifica un puerto de impresora compatible.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Estructura de PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706640"
---
# <a name="port_info_2-structure"></a>Estructura de la información de puerto \_ \_ 2

La estructura de la **información de puerto \_ \_ 2** identifica un puerto de impresora compatible.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pPortName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica un puerto de impresora compatible (por ejemplo, "LPT1:").

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica un monitor instalado (por ejemplo, "monitor PJL"). Puede ser **null**.

</dd> <dt>

**pDescription**
</dt> <dd>

Puntero a una cadena terminada en null que describe el puerto con más detalle (por ejemplo, si **pPortName** es "LPT1:", **pDescription** es "Puerto de impresora"). Puede ser **null**.

</dd> <dt>

**fPortType**
</dt> <dd>

Máscara de máscara que describe el tipo de puerto. Este miembro puede ser una combinación de los siguientes valores:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**tipo de puerto \_ \_ Write**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**tipo de puerto \_ \_ leído**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**tipo de puerto \_ \_ Redirigido**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**tipo de puerto \_ \_ conectado a red \_**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use la estructura de la **información de puerto \_ \_ 2** al llamar a [**EnumPorts**](enumports.md) si hay varios monitores instalados que admitan los mismos puertos.

El miembro **fPortType** se puede consultar para determinar la información sobre el puerto. Tenga en cuenta que la configuración del puerto no afecta a los atributos de la impresora (devueltos por el miembro **attributes** de la información de la [**impresora \_ \_ 2**](printer-info-2.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Port \_ info \_ 2W** (Unicode) y la **\_ información de puerto \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




