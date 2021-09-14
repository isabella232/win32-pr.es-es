---
description: Hay varias funciones que cambian la instalación de componentes y características del producto. A continuación se describe cómo cambiar características y componentes.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Trabajar con características y componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253964"
---
# <a name="working-with-features-and-components"></a>Trabajar con características y componentes

Hay varias funciones que cambian la instalación de componentes [y características del producto.](components-and-features.md) A continuación se describe cómo cambiar características y componentes.

**Para cambiar la instalación de características y componentes**

1.  Establezca el nivel de instalación de un componente o característica mediante una llamada a [**la función MsiSetInstallLevel.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)

    A cada característica de un paquete se le asigna un nivel de instalación en la [tabla Característica](feature-table.md). Si el nivel de instalación de una característica es inferior al nivel establecido por [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la característica se selecciona para la instalación. Después **de llamar a MsiSetInstallLevel,** puede cambiar explícitamente si una característica está instalada.

2.  Determine qué estados están disponibles para una característica especificada llamando a la [**función MsiGetFeatureValidStates.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
3.  Obtenga los requisitos de espacio en disco para una característica especificada y sus características secundarias mediante una llamada a la [**función MsiGetFeatureCost.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
4.  Obtenga el estado actual de una característica o componente mediante una llamada a la función [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o a [**la función MsiGetComponentState.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
5.  Cambie el estado de la característica o componente con la función [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o [**la función MsiSetComponentState.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)

 

 



