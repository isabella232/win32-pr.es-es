---
title: Resolución de varios componentes de agregación que admiten la misma interfaz
description: No es habitual que dos extensiones expongan la misma interfaz a ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Resolución de varios componentes de agregación que admiten la misma interfaz ADSI
- resolución de varios componentes de agregación que admiten la misma interfaz ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656157"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Resolución de varios componentes de agregación que admiten la misma interfaz

No es habitual que dos extensiones expongan la misma interfaz a ADSI. Si esto ocurre, se aplican las siguientes reglas:

-   Si una interfaz, como **IMyInterface**, es compatible con el agregador (ADSI) y cualquier objeto de extensión, **QueryInterface** siempre devuelve el **IMyInterface** de ADSI.
-   Si el agregador (ADSI) no admite una interfaz, como **IMyInterface**, pero es compatible con más de un objeto de extensión, **QueryInterface** devuelve el **IMyInterface** del primer objeto de extensión enumerado en el registro que admite la interfaz.

Tenga en cuenta que el orden de los componentes del registro también afecta a la resolución de conflictos de nombres en la automatización. Para obtener más información, consulte [resolución de conflictos de nombres de función y propiedad en Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).

 

 




