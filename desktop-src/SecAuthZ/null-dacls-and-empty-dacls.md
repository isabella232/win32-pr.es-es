---
description: Una DACL null concede acceso completo a cualquier usuario que lo solicite. Una DACL vacía es una DACL inicializada y asignada correctamente que no contiene entradas de control de acceso. Una DACL vacía no concede ningún acceso al objeto al que se asigna.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL NULL y listas DACL vacías (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668393"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACL NULL y listas DACL vacías (autorización)

Si la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que pertenece al [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) de un objeto se establece en **null**, se crea una DACL null. Una DACL null concede acceso completo a cualquier usuario que lo solicite; la comprobación de seguridad normal no se realiza con respecto al objeto. Una DACL null no se debería confundir con una DACL vacía. Una DACL vacía es una DACL inicializada y asignada correctamente que no contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE). Una DACL vacía no concede ningún acceso al objeto al que se asigna.

Para obtener un ejemplo de cómo crear una DACL, vea [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
