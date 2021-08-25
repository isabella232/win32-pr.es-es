---
description: La sintaxis de mensajes criptográficos (CMS), derivada de PKCS 7 versión 1.5, es la sintaxis que se usa para crear hash, firmar digitalmente, autenticar y cifrar mensajes \# arbitrarios.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Adiciones de CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce7c54867c1ee2a603e37751bf43a0abc65cee670c4a1fc994c9ace3f3404bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876965"
---
# <a name="cms-additions"></a>Adiciones de CMS

La sintaxis de mensajes criptográficos (CMS), derivada de PKCS 7 versión 1.5, es la sintaxis que se usa para crear \# [*un hash,*](../secgloss/h-gly.md)firmar [*digitalmente,*](../secgloss/d-gly.md)autenticar y cifrar mensajes arbitrarios. Siempre que sea posible, se conserva la compatibilidad con versiones anteriores; sin embargo, se han realizado cambios para dar cabida a las técnicas de transferencia de certificados de atributos y contratos de claves para la administración de claves. CMS permite varias encapsulaciones para que un sobre de encapsulación se pueda anidar dentro de otro. Además, una parte puede firmar digitalmente datos encapsulados previamente; atributos arbitrarios, como el tiempo de firma, se pueden firmar junto con el contenido del mensaje; Los atributos y , como [*countersignatures*](../secgloss/c-gly.md), se pueden asociar a una firma. CMS puede admitir diversas arquitecturas para la administración de claves basada en certificados.

Para admitir funcionalidades de CMS adicionales, se han dado nuevos campos a las estructuras de datos subyacentes. También se han agregado nuevas marcas y valores de parámetro. Todas las estructuras de datos y todas las API que usan CMS son 100 % compatibles con la versión 1.5 de PKCS \# 7.

Las adiciones [incluyen adiciones de datos con sobre y](enveloped-data-additions.md) [adiciones de datos firmados.](signed-data-additions.md)

 

 
