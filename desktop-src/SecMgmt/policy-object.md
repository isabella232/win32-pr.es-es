---
description: El objeto Policy se usa para controlar el acceso a la base de datos de autoridad de seguridad local (LSA) y contiene información que se aplica a todo el sistema o establece valores predeterminados para el sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Objeto de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170822"
---
# <a name="policy-object"></a>Objeto de directiva

El **objeto Policy** se usa para controlar el acceso a la base de datos de autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) y contiene información que se aplica a todo el sistema o establece valores predeterminados para el sistema. Cada sistema solo tiene un **objeto Policy.** El **LSA** crea este objeto de directiva cuando se inicia el sistema y las aplicaciones no pueden crearlo ni destruirlo.

La información almacenada en un **objeto Policy** incluye:

-   Cuota de memoria predeterminada del sistema. A menos que se especifique lo contrario, a cada usuario que inicia sesión en el sistema se le asignará esta cuota de memoria. Las cuotas de memoria especiales se pueden asignar a individuos o miembros de grupos o grupos locales a través de un [**objeto Account.**](account-object.md)
-   Requisitos de auditoría de seguridad en todo el sistema.
-   Nombre y SID del dominio de cuenta de este sistema.
-   Información sobre el dominio principal de este sistema. Esta información incluye el nombre y el SID del dominio principal, el nombre de la cuenta dentro del dominio principal que se va a usar para las solicitudes de autenticación, el nombre y las traducciones de SID, y la obtención de los nombres de los controladores de dominio dentro del dominio. Estos nombres pueden no estar actualizados y solo deben tomarse como una sugerencia. Se supone que el orden de esta lista es significativo y se mantendrá. Esto permite, por ejemplo, que el nombre de la lista represente el último controlador de dominio principal conocido.
-   Información sobre si el LSA contiene la copia maestra de la información de directiva o una réplica. Solo se replica parte de la información de la directiva; el resto se establece por sistema.

Los **campos AccountDomain** y **PrimaryDomain** del objeto **Policy** se usan para distintos propósitos en función del tipo de relaciones de confianza y sistema:

-   En un sistema que no tiene un dominio principal, el campo **AccountDomain** contiene el nombre y el SID del dominio de cuenta local del sistema, que es el mismo que el nombre del equipo. El **campo PrimaryDomain** contiene el nombre del grupo de trabajo del que es miembro esta máquina. [**Los objetos TrustedDomain**](trusteddomain-object.md) se omiten con una excepción: no puede haber un objeto **TrustedDomain** con el mismo nombre que el grupo de trabajo porque aparecerá como si fuera el dominio principal de la máquina.
-   En un sistema que tiene un dominio principal, el **campo AccountDomain** identifica el nombre y el SID del dominio de cuenta local, como antes. Sin embargo, **el campo PrimaryDomain** contiene el nombre y el SID del dominio principal del sistema. Además, debe haber un objeto [**TrustedDomain**](trusteddomain-object.md) con el nombre y el SID identificados en el **campo PrimaryDomain.** Este **objeto TrustedDomain** contiene la información de cuenta y servidor necesaria para establecer un canal seguro para un controlador de dominio en el dominio principal. Cualquier otro **objeto TrustedDomain** se omite.
-   En los controladores de dominio, **el campo AccountDomain** identifica el dominio de cuenta local para el sistema; sin embargo, el nombre de la cuenta se asigna al usuario en lugar de ser un nombre conocido. Puesto que el dominio principal es el mismo que el dominio de cuenta, el **campo PrimaryDomain** debe contener el mismo valor que el **campo AccountDomain.** Además, se espera que todos los objetos [**TrustedDomain**](trusteddomain-object.md) sean válidos y representen relaciones de confianza con otros dominios. Si el sistema no confía en ningún otro dominio, no debe haber ningún **objeto TrustedDomain.**

 

 
