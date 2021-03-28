---
description: En este tema se explica cómo controlar la visibilidad de los verbos.
title: Cómo suprimir y controlar la visibilidad de los verbos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276744"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a>Cómo suprimir y controlar la visibilidad de los verbos

En este tema se explica cómo controlar la visibilidad de los verbos.

## <a name="instructions"></a>Instrucciones


Puede usar la configuración de directiva de Windows para controlar la visibilidad de los verbos. Los verbos se pueden suprimir a través de la configuración de la Directiva agregando una subclave **SuppressionPolicy** o un valor GUID **SuppressionPolicyEx** a la subclave del registro del verbo. Establezca el valor de la subclave **SuppressionPolicy** en el identificador de la Directiva. Si la Directiva está activada, se suprimen el verbo y su entrada de menú contextual asociada. Para ver los posibles valores de ID. de Directiva, consulte la enumeración [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

 

 



