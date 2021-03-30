---
description: Hay varias funciones a las que una aplicación debe llamar para solicitar características.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Solicitar una característica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082886"
---
# <a name="requesting-a-feature"></a>Solicitar una característica

Hay varias funciones a las que una aplicación debe llamar para solicitar características. Antes de solicitar una característica, la aplicación debe asegurarse de que la característica está instalada. Si la aplicación llama a [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) antes de que la aplicación tenga acceso a una característica, la aplicación puede usar la información devuelta para mantener las métricas de uso.

**Para solicitar una característica**

1.  Llame a la función [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) si quiere determinar la disponibilidad de una característica sin incrementar el recuento de uso.
2.  Indique la intención de la aplicación de usar una característica mediante una llamada a la función [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .
3.  Determinar las ubicaciones de los archivos mediante una llamada a la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .
4.  Configure la característica mediante una llamada a la función [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .
5.  Obtener métricas de uso que la aplicación puede usar mediante una llamada a la función [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .

En el diagrama siguiente se ilustra el modelo de solicitud de características.

![modelo de solicitud de características. ](images/over2.png)

 

 



