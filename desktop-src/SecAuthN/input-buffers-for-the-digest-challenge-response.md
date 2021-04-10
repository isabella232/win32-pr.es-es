---
description: La autenticación HTTP mediante Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío. En la tabla siguiente se resumen estos búferes.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Búferes de entrada para la respuesta de desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153840"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Búferes de entrada para la respuesta de desafío de síntesis

La autenticación HTTP mediante Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío. En la tabla siguiente se resumen estos búferes.



| Número de búfer | Contiene                                                                                                                                             | Tipo de búfer                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Desafío recibido del servidor                                                                                                                   | \_token SECBUFFER                                            |
| 1             | Método HTTP                                                                                                                                          | PARÁMETROS de SECBUFFER \_                                           |
| 2             | H (entidad)                                                                                                                                            | PARÁMETROS de SECBUFFER \_                                           |
| 3             | El [*nombre de entidad*](../secgloss/s-gly.md) de seguridad de servicio (SPN) del servidor de destino. | **SECBUFFER \_ \_host de destino** \| **SECBUFFER \_ ReadOnly**      |
| 4             | Valores de token de enlaces de canal                                                                                                                        | **SECBUFFER \_ \_enlaces de canal** \| **SECBUFFER \_ ReadOnly** |



 

El búfer cero contiene el desafío de síntesis recibido del servidor en respuesta a la solicitud inicial de un recurso protegido de acceso.

El búfer 1 contiene la representación de cadena del método, como "GET" o "POST". El método se usa en el cálculo de a2, tal como se describe en [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).

Buffer 2 es el hash [*MD5*](../secgloss/m-gly.md) del cuerpo de entidad del mensaje, tal y como se describe en RFC 2617.

El búfer 3 contiene el SPN del servidor de destino en formato UTF-8 cuando se utiliza el compendio con enlaces de canal.

El búfer 4 contiene el valor del token de enlace del canal cuando se utiliza el compendio con enlaces de canal.

## <a name="input-buffers-for-sasl"></a>Búferes de entrada para SASL

Proporcione solo el cero en el búfer. Por compatibilidad con otros SSP, puede llamar a [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sin un desafío de servidor válido. En este caso, el parámetro *pInput* debe establecerse en **null**.

 

 
