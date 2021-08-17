---
description: La estructura \_ PORT INFO \_ 2 identifica un puerto de impresora compatible.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: PORT_INFO_2 estructura (Winspool.h)
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
ms.openlocfilehash: 053745ff90e022ef2ed466518a9210d6dde18d3562fdb4232d9f4d262460ea7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470945"
---
# <a name="port_info_2-structure"></a>Estructura \_ PORT INFO \_ 2

La **estructura PORT INFO \_ \_ 2** identifica un puerto de impresora compatible.

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

Puntero a una cadena terminada en NULL que identifica un puerto de impresora compatible (por ejemplo, "LPT1:").

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica un monitor instalado (por ejemplo, "monitor PJL"). Puede ser **NULL.**

</dd> <dt>

**pDescription**
</dt> <dd>

Puntero a una cadena terminada en NULL que describe el puerto con más detalle (por ejemplo, si **pPortName** es "LPT1:", **pDescription** es "puerto de impresora"). Puede ser **NULL.**

</dd> <dt>

**fPortType**
</dt> <dd>

Máscara de bits que describe el tipo de puerto. Este miembro puede ser una combinación de los valores siguientes:

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**ESCRITURA \_ DE TIPO DE \_ PUERTO**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**TIPO \_ DE PUERTO \_ READ**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**TIPO \_ DE PUERTO \_ REDIRIGIDO**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**TIPO \_ DE PUERTO CONECTADO A LA \_ \_ RED**
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use la **estructura \_ PORT INFO \_ 2** al llamar [**a EnumPorts**](enumports.md) si hay varios monitores instalados que admiten los mismos puertos.

Se puede consultar el miembro **fPortType** para determinar información sobre el puerto. Tenga en cuenta que la configuración de puertos no influye en los atributos de impresora (como devuelve **el** miembro Attributes de [**PRINTER INFO \_ \_ 2).**](printer-info-2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PORT \_ INFO \_ 2W** (Unicode) e **\_ PORT INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




