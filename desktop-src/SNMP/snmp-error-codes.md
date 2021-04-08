---
title: Códigos de error de SNMP (SNMP. h)
description: Microsoft implementa los siguientes códigos de error SNMP definidos por la especificación SNMPv2C.
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c1ec7a25490737dd31b2962c09d2e0f36c72d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078974"
---
# <a name="snmp-error-codes"></a>Códigos de error de SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

Microsoft implementa los siguientes códigos de error SNMP definidos por la especificación SNMPv2C.



| Constante o valor                                                                                                                                                                                                                                                                              | Descripción                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NoError**</dt> <dt>0</dt> </dl>                                      | El agente informa de que no se produjeron errores durante la transmisión.<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | El agente no pudo colocar los resultados de la operación SNMP solicitada en un solo mensaje SNMP.<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt> </dl>                             | La operación SNMP solicitada identificó una variable desconocida.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | La operación SNMP solicitada intentó cambiar una variable, pero especificó un error de sintaxis o de valor.<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ ERRORSTATUS de \_ solo lectura**</dt> <dt>4</dt> </dl>                                   | La operación SNMP solicitada intentó cambiar una variable que no se permitió cambiar, según el perfil de la comunidad de la variable.<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ GENERR**</dt> <dt>5</dt> </dl>                                         | Se produjo un error distinto de uno de los enumerados aquí durante la operación SNMP solicitada.<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NoAccess**</dt> <dt>6</dt> </dl>                                   | No se puede obtener acceso a la variable SNMP especificada.<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt> </dl>                                | El valor especifica un tipo que es incoherente con el tipo necesario para la variable.<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | El valor especifica una longitud incoherente con la longitud necesaria para la variable.<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | El valor contiene una codificación de notación de sintaxis abstracta uno (ASN. 1) que es incoherente con la etiqueta ASN. 1 del campo.<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ \_WRONGVALUE de ERRORSTATUS**</dt> <dt>10</dt> </dl>                            | No se puede asignar el valor a la variable.<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ nocreation**</dt> <dt>11</dt> </dl>                            | La variable no existe y el agente no puede crearla.<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt> </dl>       | El valor no es coherente con los valores de otros objetos administrados.<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | Asignar el valor a la variable requiere la asignación de recursos que no están disponibles actualmente.<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | No se ha producido ningún error de validación, pero no se ha actualizado ninguna variable.<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ \_UNDOFAILED de ERRORSTATUS**</dt> <dt>15</dt> </dl>                            | No se ha producido ningún error de validación. Se actualizaron algunas variables porque no era posible deshacer la asignación.<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | Se produjo un error de autorización.<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt> </dl>                         | La variable existe pero el agente no puede modificarla.<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt> </dl>          | La variable no existe; el agente no puede crearlo porque la instancia del objeto con nombre es incoherente con los valores de otros objetos administrados.<br/> |



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
</dt> </dl>

 

