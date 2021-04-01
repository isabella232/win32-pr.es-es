---
title: Tipos de captura de SNMPv1 (SNMP. h)
description: Los tipos de captura de SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar de la PDU de captura de SNMPv1.
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
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905621"
---
# <a name="snmpv1-trap-types"></a>SNMPv1 (tipos de captura)

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Los tipos de captura de SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar de la PDU de captura de SNMPv1.



| Constante                                                                                                                                                                                                          | Descripción                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**\_COLDSTART GENERICTRAP \_ SNMP**</dt> </dl>             | Indica una captura de inicio en frío. El agente está inicializando entidades de protocolo en el modo administrado. Puede modificar los objetos en su vista.<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**\_WARMSTART GENERICTRAP \_ SNMP**</dt> </dl>             | Indica una captura de inicio en caliente. El agente se está reinicializando, pero no modificará los objetos en su vista.<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**\_LINKDOWN GENERICTRAP \_ SNMP**</dt> </dl>                | Indica una captura de vínculo. Una interfaz adjunta ha cambiado del estado up al estado Down. La primera variable de la lista de enlaces de variables identifica la interfaz.<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**\_LINKUP GENERICTRAP \_ SNMP**</dt> </dl>                      | Indica una captura de vínculo. Una interfaz asociada ha cambiado desde el inicio hacia abajo hasta el estado activo. La primera variable de la lista de enlaces de variables identifica la interfaz.<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**\_AUTHFAILURE GENERICTRAP \_ SNMP**</dt> </dl>       | Indica una interceptación de errores de autenticación. Una entidad SNMP ha enviado un mensaje SNMP, pero se ha reclamado falsamente que pertenece a una comunidad conocida.<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**\_EGPNEIGHLOSS GENERICTRAP \_ SNMP**</dt> </dl>    | Indica una captura de pérdida del vecino EGP. Un elemento EGP del mismo nivel ha cambiado al estado inactivo. La primera variable de la lista de enlaces de variables identifica la dirección IP del homólogo EGP.<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**\_ENTERSPECIFIC GENERICTRAP \_ SNMP**</dt> </dl> | Indica una captura específica de la empresa. Se ha producido un evento extraordinario. Se identifica en el parámetro *specificTrap* con un valor específico de la empresa.<br/>               |



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

 

