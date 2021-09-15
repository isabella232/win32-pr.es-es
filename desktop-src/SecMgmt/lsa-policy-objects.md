---
description: LSA almacena información de directiva de seguridad local en un conjunto de objetos. La aplicación puede consultar o editar la directiva de seguridad local mediante el acceso a estos objetos.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objetos de directiva LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476348"
---
# <a name="lsa-policy-objects"></a>Objetos de directiva LSA

LSA almacena información de directiva de seguridad local en un conjunto de objetos. La aplicación puede consultar o editar la directiva de seguridad local mediante el acceso a estos objetos.

El conjunto consta de los cuatro objetos siguientes:

-   [La directiva](policy-object.md) contiene información de directiva global.
-   [TrustedDomain](trusteddomain-object.md) contiene información sobre un dominio de confianza.
-   [La](account-object.md) cuenta contiene información sobre una cuenta de usuario, grupo o grupo local.
-   [Los datos privados](private-data-object.md) contienen información protegida, como contraseñas de cuenta de servidor. Esta información se almacena como cadenas cifradas.

Para obtener más información sobre cómo usar las funciones de directiva LSA para administrar la información almacenada en estos objetos, vea [Uso de la directiva LSA](using-lsa-policy.md).

 

 



