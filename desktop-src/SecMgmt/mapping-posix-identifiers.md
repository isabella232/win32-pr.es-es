---
description: El subsistema POSIX debe ser capaz de traducir cualquier identificador de seguridad (SID) que encuentre en un valor de 32 bits, denominado identificador POSIX.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Asignar identificadores POSIX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabb944b543fba65942eb89d526590a5aff2c26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912253"
---
# <a name="mapping-posix-identifiers"></a>Asignar identificadores POSIX

El subsistema POSIX debe ser capaz de traducir cualquier [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que encuentre en un valor de 32 bits, denominado *identificador POSIX*. Además, debe poder clasificar el identificador como un identificador de usuario o un identificador de grupo. Para entender cómo se realiza esta asignación, echemos un vistazo primero a los SID que se deben asignar.

Los SID tienen dos componentes, el SID del dominio y el identificador relativo de la cuenta en el dominio. Por ejemplo, en el SID S-1-518364-21-43-8, el último número, 8, es el identificador relativo (RID) de la cuenta y S-1-518364-21-43 es el SID del dominio.

La información de dominio se almacena en objetos [**TrustedDomain**](trusteddomain-object.md) . Parte de la información almacenada en un objeto **TrustedDomain** es un desplazamiento de identificador POSIX que se usará para los SID dentro de ese dominio. Por ejemplo, supongamos que **TrustedDomain** se define de la siguiente manera:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

Los identificadores POSIX para las cuentas de este dominio se generarían agregando 0x130000 al identificador relativo de la cuenta. Por lo tanto, el identificador POSIX correspondiente al SID S-1-518364-21-43-8 sería 0x130008.

No todas las traducciones de ID. de POSIX hacen uso de un objeto [**TrustedDomain**](trusteddomain-object.md) . En la tabla siguiente se muestran los SID que se asignan con valores de desplazamiento conocidos.



| Source                                              | Desplazamiento de identificador POSIX |
|-----------------------------------------------------|-----------------|
| SID del dominio integrado                       | 0x20000         |
| SID del dominio de cuenta                        | 0x30000         |
| SID del dominio principal (solo en estaciones de trabajo) | 0x40000         |



 

Y, por último, otro conjunto de SID, SID de inicio de sesión, requiere un procesamiento especial. Estos valores se asignan mediante el proceso de inicio de sesión de Windows para cada sesión de inicio de sesión y tienen el formato S-1-5-5-X-Y, donde X e y se tratan como un entero grande de gran tamaño \_ que se incrementa para cada sesión de inicio de sesión. Estos SID se asignan al identificador POSIX constante 0xFFF. Para asignar el identificador POSIX 0xFFF, puede traducir el [*identificador de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que mejor se adapte a la situación, o puede usar S-1-5-5-0-0 de forma predeterminada. (Por ejemplo, si un usuario POSIX aplica la protección a un objeto y especifica FFFx, es mejor sustituir el identificador de inicio de sesión del usuario que simplemente asignar S-1-5-5-0-0).

 

 
