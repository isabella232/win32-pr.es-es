---
description: Describe cómo se protege el objeto Policy de forma predeterminada.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protección de objetos de directiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3317d9cef2a6ff1dfa29753f9a807286d62f31abb0e8c0c9d0150ee10535a1fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894075"
---
# <a name="policy-object-protection"></a>Protección de objetos de directiva

El [**objeto Policy**](policy-object.md) está protegido de forma predeterminada con la siguiente configuración:

-   El grupo local WORLD tiene acceso \_ GENERIC EXECUTE.
-   Al sistema de identificadores conocido se le concede POLICY \_ ALL \_ ACCESS.
-   El administrador local del grupo local \_ tiene acceso DE LECTURA \_ GENÉRICA, ESCRITURA GENÉRICA y EJECUCIÓN \_ \_ GENÉRICA.
-   El administrador local \_ del grupo se asigna como propietario y grupo principal de este objeto.

El [**objeto Policy**](policy-object.md) no se puede crear ni destruir.

 

 



