---
description: El objeto de Directiva se utiliza para controlar el acceso a la base de datos de la autoridad de seguridad local (LSA) y contiene información que se aplica a todo el sistema o establece valores predeterminados para el sistema.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Objeto de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907817"
---
# <a name="policy-object"></a>Objeto de Directiva

El objeto de **Directiva** se utiliza para controlar el acceso a la base de datos de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) y contiene información que se aplica a todo el sistema o establece valores predeterminados para el sistema. Cada sistema tiene un solo objeto de **Directiva** . La LSA crea este objeto de **Directiva** cuando se inicia el sistema y las aplicaciones no pueden crearlo ni destruirlo.

La información almacenada en un objeto de **Directiva** incluye:

-   Cuota de memoria predeterminada del sistema. A menos que se especifique lo contrario, a cada usuario que inicie sesión en el sistema se le asignará esta cuota de memoria. Se pueden asignar cuotas de memoria especiales a personas o miembros de grupos o grupos locales a través de un objeto de [**cuenta**](account-object.md) .
-   Requisitos de auditoría de seguridad en todo el sistema.
-   El nombre y el SID del dominio de cuenta de este sistema.
-   Información sobre el dominio principal de este sistema. Esta información incluye el nombre y el SID del dominio principal, el nombre de la cuenta en el dominio principal que se va a usar para las solicitudes de autenticación, las traducciones de nombre y SID, y la obtención de los nombres de los controladores de dominio dentro del dominio. Es posible que estos nombres no estén actualizados y solo se tomen como una sugerencia. Se supone que el orden de esta lista es significativo y se mantendrá. Esto permite, por ejemplo, el primer nombre de la lista para representar el último controlador de dominio principal conocido.
-   Información sobre si LSA contiene la copia maestra de la información de la Directiva o una réplica. Solo se replica la información de la Directiva; el resto se establece por sistema.

Los campos **AccountDomain** y **PrimaryDomain** del objeto de **Directiva** se usan para distintos propósitos según el tipo de relaciones de sistema y confianza:

-   En un sistema que no tiene un dominio principal, el campo **AccountDomain** contiene el nombre y el SID del dominio de la cuenta local del sistema, que es el mismo que el nombre del equipo. El campo **PrimaryDomain** contiene el nombre del grupo de trabajo del que es miembro esta máquina. Los objetos [**TrustedDomain**](trusteddomain-object.md) se omiten con una excepción: no puede haber un objeto **TrustedDomain** con el mismo nombre que el grupo de trabajo porque aparecerá como si fuera el dominio principal de la máquina.
-   En un sistema que tiene un dominio principal, el campo **AccountDomain** identifica el nombre y el SID del dominio de cuenta local, como antes. Sin embargo, el campo **PrimaryDomain** contiene el nombre y el SID del dominio principal del sistema. Además, debe haber un objeto [**TrustedDomain**](trusteddomain-object.md) con el nombre y el SID identificados en el campo **PrimaryDomain** . Este objeto **TrustedDomain** contiene la información de cuenta y servidor necesaria para establecer un canal seguro en un controlador de dominio en el dominio principal. Se omiten los demás objetos **TrustedDomain** .
-   En los controladores de dominio, el campo **AccountDomain** identifica el dominio de la cuenta local para el sistema; sin embargo, el nombre de cuenta es usuario asignado en lugar de ser un nombre conocido. Puesto que el dominio principal es el mismo que el dominio de la cuenta, el campo **PrimaryDomain** debe contener el mismo valor que el campo **AccountDomain** . Además, se espera que todos los objetos [**TrustedDomain**](trusteddomain-object.md) sean válidos y representen relaciones de confianza con otros dominios. Si el sistema no confía en ningún otro dominio, no debería haber ningún objeto **TrustedDomain** .

 

 
