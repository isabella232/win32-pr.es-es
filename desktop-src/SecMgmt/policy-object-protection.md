---
description: Describe cómo se protege el objeto de directiva de forma predeterminada.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protección de objetos de Directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809319"
---
# <a name="policy-object-protection"></a>Protección de objetos de Directiva

El objeto de [**Directiva**](policy-object.md) está protegido de forma predeterminada con la siguiente configuración:

-   El mundo del grupo local tiene \_ acceso de ejecución genérico.
-   Se concede a la Directiva todo el acceso al sistema de IDENTIFICADOres conocidos \_ \_ .
-   El administrador LOCAL del grupo local \_ tiene \_ acceso genérico de lectura, \_ escritura genérica y \_ ejecución genérica.
-   El administrador LOCAL \_ del grupo se asigna como propietario y grupo principal de este objeto.

No se puede crear ni destruir el objeto de [**Directiva**](policy-object.md) .

 

 



