---
title: Tipos de solicitud SNMP (SNMP. h)
description: Los tipos de solicitud SNMP se utilizan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492322"
---
# <a name="snmp-request-types"></a>Tipos de solicitudes SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Los tipos de solicitud SNMP se utilizan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.



| Constante o valor                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt> </dl>                       | Recupera el valor de los valores de las variables especificadas.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ obtener \_ siguiente**</dt> <dt> \_ \_ GETNEXT de PDU de SNMP</dt> </dl>   | Recupere el valor o los valores del sucesor lexicográfico de las variables especificadas.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ Get \_ bulk**</dt> <dt>SNMP \_ PDU \_ GetBulk e inform</dt> </dl>   | Busque y recupere varios valores con una única solicitud.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**\_prueba de \_ conjunto de extensiones SNMP \_**</dt> </dl>                                                                           | Valide los valores de las variables especificadas. Esta operación maximiza la probabilidad de una operación de escritura correcta durante la solicitud de confirmación. Para obtener más información, vea la función [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ \_ \_**</dt> conjunto de la <dt> \_ PDU \_</dt> de confirmación del conjunto de extensiones </dl> | Escriba los nuevos valores en las variables especificadas.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**\_Deshacer conjunto de extensiones SNMP \_ \_**</dt> </dl>                                                                           | Restablezca los valores de las variables especificadas a sus valores antes de la solicitud de confirmación.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**\_limpieza del \_ conjunto de extensiones SNMP \_**</dt> </dl>                                                                  | Libera los recursos asignados en las solicitudes y operaciones anteriores.<br/>                                                                                                                                                                             |



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

 

