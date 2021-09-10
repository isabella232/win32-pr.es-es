---
title: Buscar un controlador específico
description: Buscar un controlador específico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- administrador de compresión de audio (ACM), buscar controladores
- ACM (administrador de compresión de audio), buscar controladores
- Ejemplos de ACM, buscar controladores
- buscar controladores
- Función acmDriverEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370352"
---
# <a name="finding-a-specific-driver"></a>Buscar un controlador específico

Es posible que quiera que la aplicación envíe un mensaje directamente a un controlador específico o que identifique determinados controladores de la lista. Por ejemplo, es posible que quiera que la aplicación identifique los controladores que admiten filtros y, a continuación, consulte cada controlador para determinar qué etiquetas de filtro admite. Puede usar la función [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) para obtener un identificador para el controlador o controladores deseados; Este identificador se puede usar para comunicarse con ese controlador.

Tenga en cuenta que cuando una aplicación instala un controlador local para su propio uso, la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) devuelve un identificador de controlador, que se puede usar para comunicarse con el controlador. No es necesario usar **acmDriverEnum** en este caso.

 

 




