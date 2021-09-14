---
title: Tipos de variables SNMP y tipos PDU de solicitud
description: Las definiciones de algunos tipos de variables SNMP y los tipos PDU de solicitud han cambiado. El archivo Snmp.h asigna los tipos antiguos a los nuevos tipos correspondientes.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071356"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>Tipos de variables SNMP y tipos PDU de solicitud

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

Las definiciones de algunos tipos de variables SNMP y los tipos PDU de solicitud han cambiado. El archivo Snmp.h asigna los tipos antiguos a los nuevos tipos correspondientes.

## <a name="modified-snmp-variable-types"></a>Tipos de variables SNMP modificados

Debe usar los nuevos tipos de variables SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que usan el servicio SNMP de Microsoft API de Administración. En la tabla se enumeran los tipos de variables SNMP antiguos con los nuevos tipos de variable correspondientes.

| Tipo de variable anterior        | Nuevo tipo de variable |
|--------------------------|-------------------|
| DIRECCIÓN \_ IP DE ASN RFC1155 \_  | ASN \_ IPADDRESS    |
| CONTADOR \_ RFC1155 de ASN \_    | ASN \_ COUNTER32    |
| MEDIDOR \_ RFC1155 de ASN \_      | ASN \_ GAUGE32      |
| ASN \_ RFC1155 \_ TIMETICKS  | ASN \_ TIMETICKS    |
| ASN \_ RFC1155 \_ OPACO     | ASN \_ OPAQUE       |
| ASN \_ RFC1213 \_ DISPSTRING | ASN \_ OCTETSTRING  |



 

## <a name="modified-snmp-pdu-request-types"></a>Tipos de solicitud PDU SNMP modificados

Debe usar los nuevos tipos de PDU SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que usan el servicio SNMP de Microsoft API de Administración. En la tabla se enumeran los tipos de PDU snmp antiguos con los nuevos tipos de PDU correspondientes.

| Tipo de PDU anterior                 | Nuevo tipo PDU        |
|------------------------------|---------------------|
| ASN \_ RFC1157 \_ GETREQUEST     | SNMP \_ PDU \_ GET      |
| ASN \_ RFC1157 \_ GETNEXTREQUEST | SNMP \_ PDU \_ GETNEXT  |
| ASN \_ RFC1157 \_ GETRESPONSE    | RESPUESTA \_ PDU DE SNMP \_ |
| ASN \_ RFC1157 \_ SETREQUEST     | SNMP \_ PDU \_ SET      |
| ASN \_ RFC1157 \_ TRAP           | SNMP \_ PDU \_ V1TRAP   |



 

 

 