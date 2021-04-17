---
description: La sintaxis de mensajes criptográficos (CMS), derivada de PKCS \# 7 versión 1,5, es la sintaxis que se usa para el hash, firma digital, autenticación y cifrado de mensajes arbitrarios.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Adiciones de CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666825"
---
# <a name="cms-additions"></a>Adiciones de CMS

La sintaxis de mensajes criptográficos (CMS), derivada de PKCS \# 7 versión 1,5, es la sintaxis que se usa para el [*hash*](../secgloss/h-gly.md), [*firma digital*](../secgloss/d-gly.md), autenticación y cifrado de mensajes arbitrarios. Siempre que sea posible, se conserva la compatibilidad con versiones anteriores. sin embargo, se han realizado cambios para acomodar las técnicas de transferencia de certificados y de acuerdo de claves para la administración de claves. CMS permite la encapsulación múltiple para que se pueda anidar un sobre de encapsulación dentro de otro. Además, una parte puede firmar digitalmente los datos encapsulados previamente; los atributos arbitrarios, como el tiempo de firma, se pueden firmar junto con el contenido del mensaje. los atributos y, como las [*Contrafirmas*](../secgloss/c-gly.md), se pueden asociar a una firma. CMS puede admitir una variedad de arquitecturas para la administración de claves basada en certificados.

Para admitir capacidades adicionales de CMS, se han asignado nuevos campos a las estructuras de datos subyacentes. También se han agregado nuevas marcas y valores de parámetro. Todas las estructuras de datos y todas las API que usan CMS tienen un 100% de compatibilidad con versiones anteriores con PKCS \# 7, versión 1,5.

Las adiciones incluyen [adiciones de datos con envoltorio](enveloped-data-additions.md) y [adiciones de datos firmados](signed-data-additions.md).

 

 
