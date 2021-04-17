---
description: Un certificado X. 509 estándar, contiene la versión, el número de serie, el identificador del algoritmo, el nombre del emisor, el intervalo de fechas válido, el nombre del firmante, el algoritmo y la información de clave pública del sujeto y, opcionalmente, el identificador único del emisor, el identificador único del firmante y las extensiones.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificados y CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325086ab0dd46ace85745ca292bcab9bcd5324e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687257"
---
# <a name="certificates-and-cryptoapi"></a>Certificados y CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) admite el uso de certificados X. 509 tal y como se define en [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt). En esta documentación se presupone el uso de un [*certificado digital*](../secgloss/c-gly.md)X. 509 o comparable.

Un certificado X. 509 estándar contiene la siguiente información.



| Campo                | Descripción                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión              | Número de versión del certificado.                                                                                                                                                                                         |
| Número de serie        | Número de serie del certificado.                                                                                                                                                                                          |
| Identificador de algoritmo | Algoritmo de firma usado por el firmante del certificado.                                                                                                                                                                        |
| Nombre del emisor          | Nombre del emisor del certificado.                                                                                                                                                                                     |
| No antes de           | Fecha antes de la cual el certificado no es válido.                                                                                                                                                                            |
| No después de            | Fecha después de la cual el certificado no es válido.                                                                                                                                                                             |
| Nombre del firmante         | Nombre de la persona o entidad para la que se emite el certificado.                                                                                                                                                      |
| Algoritmo            | Algoritmo usado para la clave pública.                                                                                                                                                                                         |
| Clave pública de asunto   | Clave pública real (una cadena de bits).                                                                                                                                                                                          |
| IDENTIFICADOR único del emisor     | Campo opcional. Si está presente, la versión debe ser la versión 2.                                                                                                                                                                     |
| IDENTIFICADOR único del firmante    | Campo opcional. Si está presente, la versión debe ser la versión 2.                                                                                                                                                                     |
| Extensiones           | Campo opcional. Representa datos adicionales que un emisor puede querer agregar a un certificado, como la dirección de correo electrónico o la autorización para emitir certificados. Si las extensiones están presentes, la versión debe ser la versión 3.<br/> |



 

 

 
