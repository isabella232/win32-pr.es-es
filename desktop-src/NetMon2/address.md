---
description: Está obsoleto y no se debe usar.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Estructura ADDRESS (Netmon.h)
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
ms.openlocfilehash: 899d68cb4d041c032ce17ac82866488dfd443071e5368d4ba87950de66a32ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796537"
---
# <a name="address-structure"></a>Estructura ADDRESS

La **estructura ADDRESS** está obsoleta y no se debe usar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Vista de los datos expresados como una dirección MAC sin formato.

</dd> <dt>

**IPAddress**
</dt> <dd>

Vista de los datos expresados como una dirección IP sin formato.

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

Vista de los datos expresados como una dirección IP raw de Raw.

</dd> <dt>

**TocadosIPAddress**
</dt> <dd>

Vista de los datos que se expresan como una dirección IP descodificada de Trass.

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

Vista de los datos como una dirección de origen de anillo de token.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Vista de los datos como una dirección de destino de anillo de token.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de origen fddi.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Vista de los datos expresados como una dirección de destino de FDDI.

</dd> <dt>

**Marcas**
</dt> <dd>

Conjunto de marcas que modifican las propiedades de dirección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




