---
description: LSA almacena la información de la Directiva de seguridad local en un conjunto de objetos. La aplicación puede consultar o editar la Directiva de seguridad local mediante el acceso a estos objetos.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objetos de directiva de LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002075"
---
# <a name="lsa-policy-objects"></a>Objetos de directiva de LSA

LSA almacena la información de la Directiva de seguridad local en un conjunto de objetos. La aplicación puede consultar o editar la Directiva de seguridad local mediante el acceso a estos objetos.

El conjunto consta de los cuatro objetos siguientes:

-   La [Directiva](policy-object.md) contiene información global de la Directiva.
-   [TrustedDomain](trusteddomain-object.md) contiene información sobre un dominio de confianza.
-   [Cuenta](account-object.md) contiene información acerca de un usuario, grupo o cuenta de grupo local.
-   Los [datos privados](private-data-object.md) contienen información protegida, como las contraseñas de las cuentas de servidor. Esta información se almacena como cadenas cifradas.

Para obtener más información sobre cómo usar las funciones de directiva de LSA para administrar la información almacenada en estos objetos, vea uso de la [Directiva de LSA](using-lsa-policy.md).

 

 



