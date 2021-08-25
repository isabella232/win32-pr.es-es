---
description: Una DACL nula concede acceso total a cualquier usuario que lo solicite. Una DACL vacía es una DACL correctamente asignada e inicializada que no contiene entradas de control de acceso. Una DACL vacía no concede ningún acceso al objeto al que se asigna.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL null y DACL vacías (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907825"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACL null y DACL vacías (autorización)

Si la [*lista de control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) que pertenece al [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad de un objeto se establece en **NULL,** se crea una DACL nula. Una DACL nula concede acceso total a cualquier usuario que lo solicite; No se realiza la comprobación de seguridad normal con respecto al objeto . Una DACL null no se debería confundir con una DACL vacía. Una DACL vacía es una DACL correctamente asignada e inicializada que no contiene entradas de [*control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE). Una DACL vacía no concede ningún acceso al objeto al que se asigna.

Para obtener un ejemplo de cómo crear una DACL, vea [Creación de una DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

 
