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
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168002"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a>Resolución de varios componentes de agregación que admiten la misma interfaz

No es habitual que dos extensiones exponan la misma interfaz a ADSI. Si esto sucede, se aplican las siguientes reglas:

-   Si una interfaz, como **IMyInterface**, es compatible con el agregador (ADSI) y con cualquier objeto de extensión, **QueryInterface** siempre devuelve **IMyInterface** para ADSI.
-   Si una interfaz, como **IMyInterface**, no es compatible con el agregador (ADSI), pero es compatible con más de un objeto de extensión, **QueryInterface** devuelve la **IMyInterface** del primer objeto de extensión enumerado en el Registro que admite la interfaz .

Tenga en cuenta que el orden de los componentes del Registro también afecta a la resolución de conflictos de nombres en Automation. Para obtener más información, vea [Resolución de conflictos de](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)nombre de función o propiedad en Automation en extensiones .

 

 




