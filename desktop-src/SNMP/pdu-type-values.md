---
title: Valores de tipo PDU (Snmp.h)
description: Los valores de tipo PDU se usan en el campo de tipo pdu \_ de la PDU para describir su tipo.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161019"
---
# <a name="pdu-type-values"></a>Valores de tipo PDU

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Los valores de tipo PDU se usan en el **campo de \_ tipo pdu** de la PDU para describir su tipo.



| Constante                                                                                                                                                                   | Descripción                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**SNMP \_ PDU \_ GET**</dt> </dl>                | Busque y recupere un valor de una variable SNMP especificada.<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP \_ PDU \_ GETNEXT**</dt> </dl>    | Busque y recupere el valor de una variable SNMP sin conocer el nombre exacto de la variable.<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**RESPUESTA \_ PDU DE SNMP \_**</dt> </dl> | Responda a una solicitud GET de PDU de SNMP \_ o a una solicitud \_ \_ \_ GETNEXT de PDU SNMP.<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**SNMP \_ PDU \_ SET**</dt> </dl>                | Almacene un valor en una variable SNMP especificada.<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**SNMP \_ PDU \_ V1TRAP**</dt> </dl>       | Indica que el formato de la captura de PDU se ajusta al estándar SNMPv1.<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GETBULK**</dt> </dl>    | Busque y recupere varios valores con una única solicitud.<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**SNMP \_ PDU \_ INFORM**</dt> </dl>       | Indica una PDU de solicitud de informe.<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**SNMP \_ PDU \_ TRAP**</dt> </dl>             | Alerta al sistema de administración de un evento excepcional en SNMPv2C.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Snmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[Referencia de SNMP](snmp-reference.md)
</dt> <dt>

[Constantes SNMP](snmp-constants.md)
</dt> </dl>

 

