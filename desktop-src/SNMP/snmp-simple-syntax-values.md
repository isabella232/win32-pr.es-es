---
title: Valores de sintaxis simples de SNMP (Snmp.h)
description: Los valores de sintaxis simples de SNMP se usan para indicar un tipo de variable SNMP.
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
ms.openlocfilehash: 85ffcd3f8e692dec2040b2b5cc86585d0ca40dd6a664c249d922eb84a16d78fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886435"
---
# <a name="snmp-simple-syntax-values"></a>Valores de sintaxis simples de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Los valores de sintaxis simples de SNMP se usan para indicar un tipo de variable SNMP.



| Constante                                                                                                                                                                           | Descripción                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**ASN \_ INTEGER**</dt> </dl>                            | Indica una variable de entero de 32 bits con signo.<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**BITS \_ de ASN**</dt> </dl>                                     | Indica una variable que es una enumeración de bits con nombre.<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**ASN \_ OCTETSTRING**</dt> </dl>                | Indica una variable de cadena de octeto.<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**ASN \_ NULL**</dt> </dl>                                     | Indica un **valor NULL.**<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**ASN \_ OBJECTIDENTIFIER**</dt> </dl> | Indica una variable de identificador de objeto.<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**ASN \_ INTEGER32**</dt> </dl>                      | Indica un valor entero de 32 bits con signo.<br/>                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Referencia de SNMP](snmp-reference.md)
</dt> <dt>

[Constantes SNMP](snmp-constants.md)
</dt> </dl>

 

