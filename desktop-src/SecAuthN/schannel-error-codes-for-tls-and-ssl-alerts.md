---
description: Schannel devuelve los siguientes mensajes de error cuando se recibe la alerta correspondiente de los protocolos seguridad de la capa de transporte (TLS) o Capa de sockets seguros (SSL).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Códigos de error de Schannel para alertas TLS y SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4819c39948a2baf5889734fe7e2c08c8d85cbd22868cc9fad8a33281d13a306c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918594"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Códigos de error de Schannel para alertas TLS y SSL

[*Schannel*](../secgloss/s-gly.md) devuelve los siguientes mensajes de error [](../secgloss/t-gly.md) cuando se recibe la alerta correspondiente de los protocolos seguridad de la capa de transporte (TLS) o [*Capa de sockets seguros*](../secgloss/s-gly.md) (SSL). Los mensajes de error se definen en Winerror.h.



| Alerta TLS o SSL                                           | Código de error de Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| MENSAJE INESPERADO \_ DE ALERTA \_ SSL3 \_<br/> 10<br/>  | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| MAC DE REGISTRO \_ NO CIFRADO DE ALERTA \_ \_ TLS1 \_<br/> 20<br/>     | SEG \_ E \_ MESSAGE \_ ALTERED<br/> 0x8009030F<br/>             |
| ERROR DE DESCIFRADO \_ DE \_ ALERTAS TLS1 \_<br/> 21<br/>   | ERROR \_ DE DESCIFRADO POR SEGUNDO E \_ \_<br/> 0x80090330<br/>             |
| DESBORDAMIENTO DEL REGISTRO \_ DE \_ ALERTA \_ TLS1<br/> 22<br/>     | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| ERROR DE \_ \_ DESCOMPRESIÓN DE ALERTAS SSL3 \_<br/> 30<br/>  | SEG \_ E \_ MESSAGE \_ ALTERED<br/> 0x8009030F<br/>             |
| ERROR DE \_ PROTOCOLO DE ENLACE DE ALERTA \_ \_ SSL3<br/> 40<br/>   | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| CERTIFICADO NO \_ VÁLIDO DE ALERTA \_ TLS1 \_<br/> 42<br/>     | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| CERTIFICADO NO \_ ADMITIDO DE ALERTA \_ TLS1 \_<br/> 43<br/>    | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| CERTIFICADO DE \_ ALERTA \_ TLS1 \_ REVOCADO<br/> 44<br/> | CRYPT \_ E \_ REVOKED<br/> 0x80092010<br/>                    |
| CERTIFICADO DE \_ ALERTA TLS1 \_ \_ EXPIRADO<br/> 45<br/> | SEG \_ E \_ CERT \_ EXPIRED<br/> 0x80090328<br/>                |
| CERTIFICADO DE \_ ALERTA TLS1 \_ \_ DESCONOCIDO<br/> 46<br/> | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| PARÁMETRO NO \_ VÁLIDO DE ALERTA \_ SSL3 \_<br/>                 | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| ALERTA TLS1 \_ CA \_ \_ DESCONOCIDA<br/> 48<br/>          | SEC \_ E RAÍZ QUE NO ES DE \_ \_ CONFIANZA<br/> 0x80090325<br/>              |
| ACCESO DENEGADO \_ DE ALERTA \_ TLS1 \_<br/> 49<br/>       | SE \_ DENEGÓ EL \_ INICIO DE SESIÓN \_ E.<br/> 0x8009030C<br/>                |
| ERROR DE \_ DESCODIFICACIÓN \_ DE ALERTAS TLS1 \_<br/> 50<br/>        | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| ERROR DE DESCIFRADO \_ DE ALERTA \_ TLS1 \_<br/> 51<br/>       | ERROR \_ DE DESCIFRADO POR SEGUNDO E \_ \_<br/> 0x80090330<br/>             |
| RESTRICCIÓN DE EXPORTACIÓN \_ DE \_ ALERTAS TLS1 \_<br/> 60<br/>  | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| VERSIÓN DEL \_ PROTOCOLO DE \_ ALERTA TLS1 \_<br/> 70<br/>    | SEC \_ E FUNCIÓN NO \_ \_ ADMITIDA<br/> 0x80090302<br/>        |
| SEGURIDAD \_ \_ INSUFFIENT DE ALERTA TLS1 \_<br/> 71<br/> | ERROR DE \_ COINCIDENCIA DEL ALGORITMO E DE \_ \_ SEC<br/> 0x80090331<br/>          |
| ERROR INTERNO \_ DE ALERTA \_ TLS1 \_<br/> 80<br/>      | ERROR \_ INTERNO DE SEC E \_ \_<br/> 0x80090304<br/>              |
| USUARIO DE \_ ALERTA \_ TLS1 \_ CANCELADO<br/> 90<br/>       | SEG \_ E CONTEXTO SIN TERMINAR \_ \_ \_ ELIMINADO<br/> 0x80090333<br/> |
| ALERTA TLS1 \_ \_ SIN \_ RENEGOCIACIÓN<br/> 100<br/>   | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| EXT NO \_ ADMITIDO \_ DE ALERTA TLS1 \_<br/> 110<br/>    | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |
| Valor predeterminado<br/>                                         | MENSAJE \_ NO ES DE SEC E \_ \_<br/> 0x80090326<br/>             |



 

 

 
