---
description: Contiene una única dirección de cualquier tipo de direcciones admitidas.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: Estructura ADDRESS2 (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95716e7d593bdf655960bfd64901fa09c1020bc4e7d1b6ec850964311a80ca52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012373"
---
# <a name="address2-structure"></a>Estructura ADDRESS2

La **estructura ADDRESS** contiene una única dirección de cualquier tipo de direcciones admitidas.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo de dirección. Los valores pueden ser cualquier de los siguientes:

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IP6</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Vista de los datos expresados como una dirección MAC sin formato.

</dd> <dt>

**IPAddress**
</dt> <dd>

Vista de los datos expresados como una dirección IP sin formato.

</dd> <dt>

**IP6Address**
</dt> <dd>

Vista de los datos expresados como una dirección IP sin formato versión 6.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Vista de los datos expresados como una dirección IPX sin formato.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Vista de los datos expresados como un valor de dirección IPX descodificada.

</dd> <dt>

**TocadosIPRawAddress**
</dt> <dd>

Vista de los datos expresados como una dirección IP raw Desc.

</dd> <dt>

**TocadosIPAddress**
</dt> <dd>

Vista de los datos expresados como una dirección IP descodificada.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de origen Ethernet.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de destino Ethernet.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Vista de los datos como una dirección de origen del anillo de token.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Vista de los datos como una dirección de destino del anillo de token.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de origen FDDI.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de destino FDDI.

</dd> <dt>

**Marcas**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




