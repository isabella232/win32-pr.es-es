---
title: Valores de tipo de PDU (SNMP. h)
description: Los valores de tipo PDU se usan en el \_ campo de tipo PDU de la PDU para describir su tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492323"
---
# <a name="pdu-type-values"></a>Valores de tipo de PDU

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Los valores de tipo PDU se usan en el campo de **\_ tipo PDU** de la PDU para describir su tipo.



| Constante                                                                                                                                                                   | Descripción                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**\_obtención de PDU de SNMP \_**</dt> </dl>                | Busque y recupere un valor de una variable SNMP especificada.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**\_GETNEXT de PDU de SNMP \_**</dt> </dl>    | Busque y recupere el valor de una variable SNMP sin conocer el nombre exacto de la variable.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**\_respuesta de PDU de SNMP \_**</dt> </dl> | Responda a una solicitud de PDU de SNMP \_ \_ get o a una \_ solicitud GETNEXT de PDU de SNMP \_ .<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**\_conjunto de PDU de SNMP \_**</dt> </dl>                | Almacene un valor en una variable SNMP especificada.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**\_V1TRAP de PDU de SNMP \_**</dt> </dl>       | Indica que la captura de PDU tiene el formato que se ajusta al estándar SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**\_GetBulk e inform de PDU de SNMP \_**</dt> </dl>    | Busque y recupere varios valores con una única solicitud.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**\_Informe de PDU de SNMP \_**</dt> </dl>       | Indica una PDU de solicitud de informe.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**\_captura de PDU de SNMP \_**</dt> </dl>             | Avisa al sistema de administración de un evento extraordinario bajo SNMPv2C.<br/>                             |



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

 

