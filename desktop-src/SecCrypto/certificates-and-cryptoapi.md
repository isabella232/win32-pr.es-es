---
description: Un certificado estándar X.509 contiene la versión, el número de serie, el identificador del algoritmo, el nombre del emisor, el intervalo de fechas válido, el nombre del firmante, el algoritmo y la información de clave pública del firmante y, opcionalmente, el identificador único del emisor, el identificador único del firmante y las extensiones.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificados y CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8af32073cc3f42bbee07d1702fd1e6044c424ac236cf05ed8374c33757c1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770746"
---
# <a name="certificates-and-cryptoapi"></a>Certificados y CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) admite el uso de certificados X.509 tal como se define en [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt). En esta documentación se da por supuesto el uso de un certificado digital X.509 o [*comparable.*](../secgloss/c-gly.md)

Un certificado estándar X.509 contiene la siguiente información.



| Campo                | Descripción                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión              | Número de versión del certificado.                                                                                                                                                                                         |
| Número de serie        | Número de serie del certificado.                                                                                                                                                                                          |
| Identificador de algoritmo | Algoritmo de firma utilizado por el firmante del certificado.                                                                                                                                                                        |
| Nombre del emisor          | Nombre del emisor del certificado.                                                                                                                                                                                     |
| No antes de           | Fecha antes de la cual el certificado no es válido.                                                                                                                                                                            |
| No después de            | Fecha después de la cual el certificado no es válido.                                                                                                                                                                             |
| Nombre del firmante         | Nombre de la persona o entidad a la que se emite el certificado.                                                                                                                                                      |
| Algoritmo            | Algoritmo utilizado para la clave pública.                                                                                                                                                                                         |
| Clave pública del sujeto   | Clave pública real (una cadena de bits).                                                                                                                                                                                          |
| Identificador único del emisor     | Campo opcional. Si está presente, la versión debe ser la versión 2.                                                                                                                                                                     |
| Id. único del sujeto    | Campo opcional. Si está presente, la versión debe ser la versión 2.                                                                                                                                                                     |
| Extensiones           | Campo opcional. Representa datos adicionales que un emisor puede querer agregar a un certificado, como la dirección de correo electrónico o la autorización para emitir certificados. Si hay extensiones, la versión debe ser la 3.<br/> |



 

 

 
