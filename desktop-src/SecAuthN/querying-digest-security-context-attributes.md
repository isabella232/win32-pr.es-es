---
description: La función QueryContextAttributes (Digest) proporciona información sobre la configuración actual de un contexto de seguridad.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consulta de atributos de contexto de seguridad implícita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24499d5119814edec12f29cf5a39ea027f95c100626be1af1d132c952682599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919964"
---
# <a name="querying-digest-security-context-attributes"></a>Consulta de atributos de contexto de seguridad implícita

La [**función QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) proporciona información sobre la configuración actual de un [*contexto de seguridad*](../secgloss/s-gly.md).

Microsoft Digest permite consultar los siguientes atributos de contexto de seguridad.



| Atributo                   | Descripción                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECPKG \_ ATTR \_ KEY \_ INFO     | Información relacionada con los algoritmos de firma y cifrado en uso.                                                                                                                                   |
| INFORMACIÓN DEL \_ PAQUETE SECPKG ATTR \_ \_ | Información general relativa a Microsoft Digest, como el tamaño máximo de token permitido por el [*paquete de seguridad*](../secgloss/s-gly.md). |
| TAMAÑOS DE \_ SECPKG ATTR \_         | Tamaños máximos permitidos para los datos relacionados con mensajes, como las firmas.                                                                                                                                |



 

 

 
