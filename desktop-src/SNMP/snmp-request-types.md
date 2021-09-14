---
title: Tipos de solicitud SNMP (Snmp.h)
description: Los tipos de solicitud SNMP se usan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073807"
---
# <a name="snmp-request-types"></a>Tipos de solicitud SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Los tipos de solicitud SNMP se usan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.



| Constante o valor                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ GET**</dt> <dt>SNMP \_ PDU \_ GET</dt> </dl>                       | Recupere el valor de los valores de las variables especificadas.<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ GET \_ NEXT**</dt> <dt>SNMP \_ PDU \_ GETNEXT</dt> </dl>   | Recupere el valor o los valores del sucesor lexicográfico de las variables especificadas.<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_ EXTENSIÓN \_ GET \_ BULK**</dt> <dt>SNMP \_ PDU \_ GETBULK</dt> </dl>   | Busque y recupere varios valores con una única solicitud.<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**SNMP \_ EXTENSION \_ SET \_ TEST**</dt> </dl>                                                                           | Valide los valores de las variables especificadas. Esta operación maximiza la probabilidad de una operación de escritura correcta durante la solicitud COMMIT. Para obtener más información, vea la [**función SnmpExtensionQueryEx.**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex)<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_ CONJUNTO \_ DE EXTENSIONES COMMIT \_ SNMP**</dt> <dt> \_ PDU \_ SET</dt> </dl> | Escriba los nuevos valores en las variables especificadas.<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**DESHACER \_ CONJUNTO DE EXTENSIONES \_ \_ SNMP**</dt> </dl>                                                                           | Restablezca los valores de las variables especificadas a sus valores antes de la solicitud COMMIT.<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**LIMPIEZA \_ DEL CONJUNTO DE EXTENSIONES \_ \_ SNMP**</dt> </dl>                                                                  | Liberar los recursos asignados en solicitudes y operaciones anteriores.<br/>                                                                                                                                                                             |



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

 

