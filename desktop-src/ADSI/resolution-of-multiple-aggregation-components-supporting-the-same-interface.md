---
title: Resolución de varios componentes de agregación que admiten la misma interfaz
description: No es habitual que dos extensiones exponan la misma interfaz a ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Resolución de varios componentes de agregación que admiten la misma interfaz ADSI
- resolución de varios componentes de agregación que admiten la misma interfaz ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55fbc499ab3747b65ace9e869a0d5930894211d73a07ab1078eef8614694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082329"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Resolución de varios componentes de agregación que admiten la misma interfaz

No es habitual que dos extensiones exponan la misma interfaz a ADSI. Si esto sucede, se aplican las siguientes reglas:

-   Si una interfaz, como **IMyInterface**, es compatible con el agregador (ADSI) y cualquier objeto de extensión, **QueryInterface** siempre devuelve **IMyInterface** para ADSI.
-   Si una interfaz, como **IMyInterface**, no es compatible con el agregador (ADSI), pero es compatible con más de un objeto de extensión, **QueryInterface** devuelve la **IMyInterface** del primer objeto de extensión enumerado en el Registro que admite la interfaz .

Tenga en cuenta que el orden de los componentes del Registro también afecta a la resolución de conflictos de nombres en Automation. Para obtener más información, vea [Resolución de conflictos de](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)nombre de función o propiedad en Automation en extensiones .

 

 




