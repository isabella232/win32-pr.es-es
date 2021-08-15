---
description: Hay varias funciones que una aplicación debe llamar para solicitar características.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Solicitud de una característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288804168f6adf936550fee0ac0c542bd68f4d468d6aedd6372071744b9fec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990569"
---
# <a name="requesting-a-feature"></a>Solicitud de una característica

Hay varias funciones que una aplicación debe llamar para solicitar características. Antes de solicitar una característica, la aplicación debe asegurarse de que está instalada. Si la aplicación llama a [**MsiUseFeature antes**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) de que la aplicación acceda a una característica, la aplicación puede usar la información devuelta para mantener las métricas de uso.

**Para solicitar una característica**

1.  Llame a [**msiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o a la función [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) si desea determinar la disponibilidad de una característica sin incrementar el recuento de uso.
2.  Indique la intención de la aplicación de usar una característica mediante una llamada a la [**función MsiUseFeature.**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
3.  Determine las ubicaciones de archivo mediante una llamada [**a la función MsiGetComponentPath.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
4.  Configure la característica mediante una llamada a [**la función MsiConfigureFeature.**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
5.  Obtenga las métricas de uso que la aplicación puede usar llamando a la [**función MsiGetFeatureUsage.**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)

En el diagrama siguiente se muestra el modelo de solicitud de características.

![modelo de solicitud de características. ](images/over2.png)

 

 



