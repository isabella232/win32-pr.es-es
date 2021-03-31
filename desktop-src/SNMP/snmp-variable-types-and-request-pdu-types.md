---
title: Tipos de variables de SNMP y tipos PDU de solicitud
description: Las definiciones de algunos tipos de variables de SNMP y tipos PDU de solicitud han cambiado. El archivo SNMP. h asigna los tipos antiguos a los nuevos tipos correspondientes.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792867"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>Tipos de variables de SNMP y tipos PDU de solicitud

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Las definiciones de algunos tipos de variables de SNMP y tipos PDU de solicitud han cambiado. El archivo SNMP. h asigna los tipos antiguos a los nuevos tipos correspondientes.

## <a name="modified-snmp-variable-types"></a>Tipos de variables SNMP modificados

Debe usar los nuevos tipos de variables SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que utilizan la API de administración de SNMP de Microsoft. En la tabla se enumeran los tipos de variables SNMP anteriores con los nuevos tipos de variables correspondientes.

| Tipo de variable anterior        | Nuevo tipo de variable |
|--------------------------|-------------------|
| \_ \_ Dirección IP de ASN RFC1155  | \_dirección IP de ASN    |
| \_Contador RFC1155 \_ ASN    | \_COUNTER32 ASN    |
| \_Medidor de RFC1155 ASN \_      | \_GAUGE32 ASN      |
| \_TIMETICKS RFC1155 \_ ASN  | \_TIMETICKS ASN    |
| ASN \_ RFC1155 \_ opaco     | opaco de ASN \_       |
| \_DISPSTRING RFC1213 \_ ASN | \_OCTETSTRING ASN  |



 

## <a name="modified-snmp-pdu-request-types"></a>Tipos de solicitud de PDU de SNMP modificados

Debe usar los nuevos tipos de PDU de SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que utilizan la API de administración de SNMP de Microsoft. En la tabla se enumeran los tipos de PDU de SNMP antiguos con los nuevos tipos PDU correspondientes.

| Tipo de PDU anterior                 | Nuevo tipo de PDU        |
|------------------------------|---------------------|
| \_GETREQUEST RFC1157 \_ ASN     | \_obtención de PDU de SNMP \_      |
| \_GETNEXTREQUEST RFC1157 \_ ASN | \_GETNEXT de PDU de SNMP \_  |
| ASN \_ RFC1157 \_ GETRESPONSE    | \_respuesta de PDU de SNMP \_ |
| \_SETREQUEST RFC1157 \_ ASN     | \_conjunto de PDU de SNMP \_      |
| \_Captura de RFC1157 ASN \_           | \_V1TRAP de PDU de SNMP \_   |



 

 

 