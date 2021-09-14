---
description: El subsistema Posix debe ser capaz de traducir cualquier identificador de seguridad (SID) que encuentre en un valor de 32 bits, denominado id. de Posix.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Asignación de identificadores posix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073601"
---
# <a name="mapping-posix-identifiers"></a>Asignación de identificadores posix

El subsistema Posix debe ser [](/windows/desktop/SecGloss/s-gly) capaz de traducir cualquier identificador de seguridad (SID) que encuentre en un valor de 32 bits, denominado *id. de Posix.* Además, debe ser capaz de clasificar el identificador como un identificador de usuario o un identificador de grupo. Para comprender cómo se realiza esta asignación, veamos primero los SID que se deben asignar.

Los SID tienen dos componentes, el SID del dominio y el identificador relativo de la cuenta en el dominio. Por ejemplo, en el SID S-1-518364-21-43-8, el último número, 8, es el identificador relativo de la cuenta (RID) y S-1-518364-21-43 es el SID del dominio.

La información de dominio se almacena en [**objetos TrustedDomain.**](trusteddomain-object.md) Parte de la información almacenada en un **objeto TrustedDomain** es un desplazamiento de id. de Posix que se usará para los SID dentro de ese dominio. Por ejemplo, suponga que **trustedDomain** está definido de la siguiente manera:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

Los identificadores de Posix para las cuentas de este dominio se generarían agregando 0x130000 al identificador relativo de la cuenta. Por lo tanto, el identificador de Posix correspondiente al SID S-1-518364-21-43-8 sería 0x130008.

No todas las traducciones de id. de Posix usan un [**objeto TrustedDomain.**](trusteddomain-object.md) En la tabla siguiente se muestran los SID que se asignan mediante valores de desplazamiento conocidos.



| Source                                              | Desplazamiento de id. de Posix |
|-----------------------------------------------------|-----------------|
| SID del dominio integrado                       | 0x20000         |
| SID del dominio de cuenta                        | 0x30000         |
| SID del dominio principal (solo en estaciones de trabajo) | 0x40000         |



 

Por último, otro conjunto de SID, SID de inicio de sesión, requiere un procesamiento especial. El proceso de inicio de sesión de Windows asigna estos valores para cada sesión de inicio de sesión y tienen el formato S-1-5-5-X-Y, donde X e Y se tratan como un único ENTERO GRANDE que se incrementa para cada sesión de inicio de \_ sesión. Estos SID se asignan a la constante Posix ID 0xFFF. Para asignar el identificador de Posix 0xFFF, [](/windows/desktop/SecGloss/l-gly) puede traducir el identificador de inicio de sesión que mejor se adapte a la situación, o bien puede usar S-1-5-5-0-0 de forma predeterminada. (Por ejemplo, si un usuario posix aplica protección a un objeto y especifica FFFx, es mejor sustituir el identificador de inicio de sesión de ese usuario que simplemente asignar S-1-5-5-0-0).

 

 
