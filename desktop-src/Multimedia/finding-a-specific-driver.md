---
title: Búsqueda de un controlador específico
description: Búsqueda de un controlador específico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Administrador de compresión de audio (ACM), buscar controladores
- ACM (Administrador de compresión de audio), buscar controladores
- Ejemplos de ACM, buscar controladores
- Buscar controladores
- acmDriverEnum función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903779"
---
# <a name="finding-a-specific-driver"></a>Búsqueda de un controlador específico

Es posible que desee que la aplicación envíe un mensaje directamente a un controlador específico o que identifique determinados controladores de la lista. Por ejemplo, puede que desee que la aplicación identifique los controladores que admiten filtros y, a continuación, consulte cada controlador para determinar las etiquetas de filtro que admite. Puede usar la función [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) para obtener un identificador para el controlador o los controladores que desee; Este identificador se puede usar para comunicarse con el controlador.

Tenga en cuenta que cuando una aplicación instala un controlador local para su propio uso, la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) devuelve un identificador de controlador, que se puede usar para comunicarse con el controlador. En este caso, no es necesario usar **acmDriverEnum** .

 

 




