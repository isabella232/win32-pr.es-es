---
description: La autenticación HTTP Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío. En la tabla siguiente se resumen estos búferes.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Búferes de entrada para la respuesta del desafío de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071283"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a>Búferes de entrada para la respuesta del desafío de resumen

La autenticación HTTP Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío. En la tabla siguiente se resumen estos búferes.



| Número de búfer | Contiene                                                                                                                                             | Tipo de búfer                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| 0             | Desafío recibido del servidor                                                                                                                   | TOKEN DE SECBUFFER \_                                            |
| 1             | Método HTTP                                                                                                                                          | SECBUFFER \_ PARAMS                                           |
| 2             | H(Entidad)                                                                                                                                            | SECBUFFER \_ PARAMS                                           |
| 3             | Nombre [*de entidad de seguridad*](../secgloss/s-gly.md) de servicio (SPN) del servidor de destino. | **SECBUFFER \_ HOST \_ DE DESTINO** \| **SECBUFFER \_ READONLY**      |
| 4             | Valores de token de enlaces de canal                                                                                                                        | **SECBUFFER \_ ENLACES \_ DE CANAL** \| **SECBUFFER \_ READONLY** |



 

El búfer cero contiene el desafío Digest recibido del servidor en respuesta a la solicitud inicial de un recurso protegido por acceso.

El búfer 1 contiene la representación de cadena del método, como "GET" o "POST". El método se usa en el cálculo de A2, como se describe en [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).

El búfer 2 es el hash [*MD5*](../secgloss/m-gly.md) del cuerpo de la entidad del mensaje, tal como se describe en RFC 2617.

El búfer 3 contiene el SPN del servidor de destino en formato UTF-8 cuando se usa digest con enlaces de canal.

El búfer 4 contiene el valor del token de enlace de canal cuando se usa Digest con enlaces de canal.

## <a name="input-buffers-for-sasl"></a>Búferes de entrada para SASL

Proporcione solo el búfer cero. Por compatibilidad con otros SSP, puede llamar a [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sin un desafío de servidor válido. En este caso, *el parámetro pInput* debe establecerse en **NULL.**

 

 
