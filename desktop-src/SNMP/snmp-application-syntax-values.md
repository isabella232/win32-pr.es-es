---
title: Valores de sintaxis de la aplicación SNMP (SNMP. h)
description: Las aplicaciones de administración que emplean la API de administración de SNMP de Microsoft usan los valores de sintaxis de la aplicación SNMP.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150165"
---
# <a name="snmp-application-syntax-values"></a>Valores de sintaxis de la aplicación SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Las aplicaciones de administración que emplean la API de administración de SNMP de Microsoft usan los valores de sintaxis de la aplicación SNMP.



| Constante                                                                                                                                                                                  | Descripción                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**\_dirección IP de ASN**</dt> </dl>                             | Indica una variable de dirección IP.<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**\_COUNTER32 ASN**</dt> </dl>                             | Indica una variable de contador.<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**\_GAUGE32 ASN**</dt> </dl>                                   | Indica una variable de medidor. Esta variable describe un tipo Unsigned32 en conformidad con RFC 1902.<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**\_TIMETICKS ASN**</dt> </dl>                             | Indica una variable timeticks.<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**opaco de ASN \_**</dt> </dl>                                      | Indica una variable opaca.<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**\_COUNTER64 ASN**</dt> </dl>                             | Indica una variable de contador que aumenta hasta que alcanza un valor máximo de (2 ^ 64)-1.<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**\_UINTEGER32 ASN**</dt> </dl>                          | Indica una variable de entero de 32 bits sin signo. Esta variable describe un tipo UInteger32 en conformidad con RFC 1442.<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt> </dl> | Consulte ASN \_ GAUGE32.<br/>                                                                                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                              |
| Encabezado<br/>                   | <dl> <dt>SNMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Referencia de SNMP](snmp-reference.md)
</dt> <dt>

[Constantes de SNMP](snmp-constants.md)
</dt> </dl>

 

