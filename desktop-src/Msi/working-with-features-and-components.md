---
description: Hay varias funciones que cambian la instalación de componentes y características del producto. A continuación se describe cómo cambiar características y componentes de.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Trabajar con características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678023"
---
# <a name="working-with-features-and-components"></a>Trabajar con características y componentes

Hay varias funciones que cambian la instalación de [componentes y características](components-and-features.md)del producto. A continuación se describe cómo cambiar características y componentes de.

**Para cambiar la instalación de características y componentes**

1.  Establezca el nivel de instalación de un componente o característica mediante una llamada a la función [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .

    A cada característica de un paquete se le asigna un nivel de instalación en la [tabla de características](feature-table.md). Si el nivel de instalación de una característica es inferior al nivel establecido por [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la característica se selecciona para su instalación. Después de llamar a **MsiSetInstallLevel** , puede cambiar explícitamente si una característica está instalada.

2.  Determine qué Estados están disponibles para una característica determinada llamando a la función [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .
3.  Obtener los requisitos de espacio en disco para una característica especificada y sus características secundarias mediante una llamada a la función [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .
4.  Obtenga el estado actual de una característica o componente mediante una llamada a la función [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o a la función [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .
5.  Cambiar el estado de la característica o componente con la función [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o la función [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .

 

 



