---
description: Está obsoleto y no debe usarse.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Estructura de dirección (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667550"
---
# <a name="address-structure"></a>Estructura de dirección

La estructura de la **Dirección** está obsoleta y no debe usarse.

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

**Mac**
</dt> <dd>

Vista de los datos expresada como una dirección MAC sin procesar.

</dd> <dt>

**IPAddress**
</dt> <dd>

Vista de los datos expresada como una dirección IP sin procesar.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Vista de los datos expresada como una dirección IPX sin procesar.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Vista de los datos expresada como un valor de dirección IPX descodificada.

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

Vista de los datos expresada como una dirección IP de Vines sin procesar.

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

Vista de los datos expresada como una dirección IP de Vines descodificada.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Vista de los datos expresada como una dirección de origen Ethernet.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Vista de los datos expresada como una dirección de destino Ethernet.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Una vista de los datos como una dirección de origen de token ring.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Una vista de los datos como una dirección de destino de token ring.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Vista de los datos expresada como una dirección de origen FDDI.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Vista de los datos expresada como una dirección de destino FDDI.

</dd> <dt>

**Marcas**
</dt> <dd>

Un conjunto de marcas que modifican las propiedades de dirección.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




