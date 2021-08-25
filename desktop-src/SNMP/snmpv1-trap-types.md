---
title: Tipos de captura SNMPv1 (Snmp.h)
description: Los tipos de captura SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar PDU de captura SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7067a6bf5aa1ea11135279484cb74722b8bcc197b507f6bba9b30e35630a2861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886245"
---
# <a name="snmpv1-trap-types"></a>Tipos de captura SNMPv1

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Los tipos de captura SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar PDU de captura SNMPv1.



| Constante                                                                                                                                                                                                          | Descripción                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | Indica una captura de arranque en frío. El agente está inicializando entidades de protocolo en el modo administrado. Puede modificar objetos en su vista.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | Indica una captura de inicio en caliente. El agente se reinicializa a sí mismo, pero no modificará los objetos en su vista.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | Indica una captura de vínculo hacia abajo. Una interfaz adjunta ha cambiado del estado de arriba al de abajo. La primera variable de la lista de enlaces de variables identifica la interfaz .<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**VÍNCULO \_ DE SNMP GENERICTRAP \_**</dt> </dl>                      | Indica una captura de vínculo hacia arriba. Una interfaz adjunta ha cambiado desde el inicio hacia abajo hasta el estado up. La primera variable de la lista de enlaces de variables identifica la interfaz .<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | Indica una captura de error de autenticación. Una entidad SNMP ha enviado un mensaje SNMP, pero ha declarado falsamente que pertenece a una comunidad conocida.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | Indica una captura de pérdida de vecino de EGP. Un elemento del mismo nivel de EGP ha cambiado al estado de bajada. La primera variable de la lista de enlaces de variables identifica la dirección IP del par EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt> </dl> | Indica una captura específica de la empresa. Se ha producido un evento excepcional. Se identifica en el *parámetro specificTrap* con un valor específico de la empresa.<br/>               |



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

 

