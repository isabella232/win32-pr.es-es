---
description: La función QueryContextAttributes (Digest) proporciona información sobre la configuración actual de un contexto de seguridad.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consulta de atributos de contexto de seguridad implícita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069138"
---
# <a name="querying-digest-security-context-attributes"></a>Consulta de atributos de contexto de seguridad implícita

La [**función QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) proporciona información sobre la configuración actual de un [*contexto de seguridad*](../secgloss/s-gly.md).

Microsoft Digest permite consultar los siguientes atributos de contexto de seguridad.



| Atributo                   | Descripción                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECPKG \_ ATTR \_ KEY \_ INFO     | Información relacionada con los algoritmos de firma y cifrado en uso.                                                                                                                                   |
| INFORMACIÓN DEL \_ PAQUETE SECPKG ATTR \_ \_ | Información general relativa a Microsoft Digest, como el tamaño máximo de token permitido por el paquete [*de seguridad*](../secgloss/s-gly.md). |
| TAMAÑOS DE \_ SECPKG ATTR \_         | Tamaños máximos permitidos para los datos relacionados con mensajes, como las firmas.                                                                                                                                |



 

 

 
