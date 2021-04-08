---
description: La función QueryContextAttributes (síntesis) proporciona información sobre la configuración actual de un contexto de seguridad.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Consultar los atributos de contexto de seguridad implícita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001858"
---
# <a name="querying-digest-security-context-attributes"></a>Consultar los atributos de contexto de seguridad implícita

La función [**QueryContextAttributes (síntesis)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) proporciona información sobre la configuración actual de un [*contexto de seguridad*](../secgloss/s-gly.md).

Microsoft Digest admite la consulta de los siguientes atributos de contexto de seguridad.



| Atributo                   | Descripción                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| información de clave de SECPKG \_ ATTR \_ \_     | Información relacionada con los algoritmos de firma y cifrado en uso.                                                                                                                                   |
| información de paquete de SECPKG \_ ATTR \_ \_ | Información general relativa a Microsoft Digest, como el tamaño máximo del token permitido por el [*paquete de seguridad*](../secgloss/s-gly.md). |
| tamaños de SECPKG \_ ATTR \_         | Los tamaños máximos permitidos para los datos relacionados con mensajes, como las firmas.                                                                                                                                |



 

 

 
