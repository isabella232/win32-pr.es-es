---
title: Valores de sintaxis simple SNMP (SNMP. h)
description: Los valores de sintaxis simple de SNMP se utilizan para indicar un tipo de variable SNMP.
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150517"
---
# <a name="snmp-simple-syntax-values"></a>Valores de sintaxis simple de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Los valores de sintaxis simple de SNMP se utilizan para indicar un tipo de variable SNMP.



| Constante                                                                                                                                                                           | Descripción                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**\_entero ASN**</dt> </dl>                            | Indica una variable de entero con signo de 32 bits.<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**\_bits ASN**</dt> </dl>                                     | Indica una variable que es una enumeración de bits con nombre.<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**\_OCTETSTRING ASN**</dt> </dl>                | Indica una variable de cadena de octeto.<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**\_nulo ASN**</dt> </dl>                                     | Indica un valor **null** .<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**\_OBJECTIDENTIFIER ASN**</dt> </dl> | Indica una variable de identificador de objeto.<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**\_INTEGER32 ASN**</dt> </dl>                      | Indica un valor entero con signo de 32 bits.<br/>                   |



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

 

