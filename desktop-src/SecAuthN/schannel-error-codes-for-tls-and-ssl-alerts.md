---
description: Schannel devuelve los mensajes de error siguientes cuando se recibe la alerta correspondiente de los protocolos de seguridad de la capa de transporte (TLS) o Capa de sockets seguros (SSL).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Códigos de error de Schannel para alertas TLS y SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fdba202e63d212fc85f0c02eb5ac9dc20db047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001849"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Códigos de error de Schannel para alertas TLS y SSL

[*Schannel*](../secgloss/s-gly.md) devuelve los mensajes de error siguientes cuando se recibe la alerta correspondiente de los protocolos de seguridad de la [*capa de transporte*](../secgloss/t-gly.md) (TLS) o [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL). Los mensajes de error se definen en Winerror. h.



| Alerta de TLS o SSL                                           | Código de error Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| Mensaje de alerta de SSL3 \_ \_ inesperado \_<br/> 10<br/>  | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| TLS1 de \_ alerta de \_ \_ registro incorrecto de alerta \_<br/> 20<br/>     | s \_ E \_ mensaje \_ modificado<br/> 0x8009030F<br/>             |
| \_Error de \_ descifrado de alerta de TLS1 \_<br/> 21<br/>   | s \_ E \_ descifrar \_ error<br/> 0x80090330<br/>             |
| \_Desbordamiento de \_ registro de alerta de TLS1 \_<br/> 22<br/>     | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| \_Error de \_ descompresión de alertas SSL3 \_<br/> 30<br/>  | s \_ E \_ mensaje \_ modificado<br/> 0x8009030F<br/>             |
| \_Error de \_ Protocolo de enlace de alertas SSL3 \_<br/> 40<br/>   | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| \_ \_ Certificado incorrecto de alerta de TLS1 \_<br/> 42<br/>     | s \_ E \_ certificado \_ desconocido<br/> 0x80090327<br/>                |
| Certificado de alerta de TLS1 \_ \_ no compatible \_<br/> 43<br/>    | s \_ E \_ certificado \_ desconocido<br/> 0x80090327<br/>                |
| Certificado de alerta de TLS1 \_ \_ \_ revocado<br/> 44<br/> | CIFRAdo \_ E \_ revocado<br/> 0x80092010<br/>                    |
| El \_ certificado de alerta TLS1 \_ \_ expiró<br/> 45<br/> | s \_ E \_ certificado \_ expirado<br/> 0x80090328<br/>                |
| Certificado de alerta de TLS1 \_ \_ \_ desconocido<br/> 46<br/> | s \_ E \_ certificado \_ desconocido<br/> 0x80090327<br/>                |
| \_Parámetro de alerta SSL3 \_ no válido \_<br/>                 | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| TLS1 \_ \_ CA desconocida \_<br/> 48<br/>          | raíz de s \_ E no \_ confiable \_<br/> 0x80090325<br/>              |
| TLS1 \_ \_ acceso \_ denegado de alerta<br/> 49<br/>       | s \_ E \_ Inicio de sesión \_ denegado<br/> 0X8009030c al<br/>                |
| \_Error de \_ descodificación de alerta de TLS1 \_<br/> 50<br/>        | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| \_Error de \_ descifrado de alerta de TLS1 \_<br/> 51<br/>       | s \_ E \_ descifrar \_ error<br/> 0x80090330<br/>             |
| \_Restricción de \_ exportación de alerta de TLS1 \_<br/> 60<br/>  | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| \_Versión del \_ Protocolo de alerta de TLS1 \_<br/> 70<br/>    | SEC \_ E \_ función no admitida \_<br/> 0x80090302<br/>        |
| TLS1 \_ alerta \_ insuficientes \_ Security<br/> 71<br/> | s \_ E \_ \_ no coinciden los algoritmos<br/> 0x80090331<br/>          |
| \_ \_ Error interno de alerta de TLS1 \_<br/> 80<br/>      | s \_ E \_ interno \_ error<br/> 0x80090304<br/>              |
| Usuario de alerta de TLS1 \_ \_ \_ cancelado<br/> 90<br/>       | s \_ E \_ contexto sin terminar \_ \_ eliminado<br/> 0x80090333<br/> |
| Alerta de TLS1 \_ \_ no \_ renegociación<br/> 100<br/>   | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| EXT. alerta de TLS1 \_ \_ no admitida \_<br/> 110<br/>    | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |
| Valor predeterminado<br/>                                         | s \_ E \_ mensaje no válido \_<br/> 0x80090326<br/>             |



 

 

 
