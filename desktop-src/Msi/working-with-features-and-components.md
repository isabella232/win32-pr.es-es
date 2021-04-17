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
# <a name="working-with-features-and-components"></a><span data-ttu-id="f8619-104">Trabajar con características y componentes</span><span class="sxs-lookup"><span data-stu-id="f8619-104">Working with Features and Components</span></span>

<span data-ttu-id="f8619-105">Hay varias funciones que cambian la instalación de [componentes y características](components-and-features.md)del producto.</span><span class="sxs-lookup"><span data-stu-id="f8619-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="f8619-106">A continuación se describe cómo cambiar características y componentes de.</span><span class="sxs-lookup"><span data-stu-id="f8619-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="f8619-107">**Para cambiar la instalación de características y componentes**</span><span class="sxs-lookup"><span data-stu-id="f8619-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="f8619-108">Establezca el nivel de instalación de un componente o característica mediante una llamada a la función [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .</span><span class="sxs-lookup"><span data-stu-id="f8619-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="f8619-109">A cada característica de un paquete se le asigna un nivel de instalación en la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f8619-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="f8619-110">Si el nivel de instalación de una característica es inferior al nivel establecido por [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la característica se selecciona para su instalación.</span><span class="sxs-lookup"><span data-stu-id="f8619-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="f8619-111">Después de llamar a **MsiSetInstallLevel** , puede cambiar explícitamente si una característica está instalada.</span><span class="sxs-lookup"><span data-stu-id="f8619-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="f8619-112">Determine qué Estados están disponibles para una característica determinada llamando a la función [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .</span><span class="sxs-lookup"><span data-stu-id="f8619-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="f8619-113">Obtener los requisitos de espacio en disco para una característica especificada y sus características secundarias mediante una llamada a la función [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .</span><span class="sxs-lookup"><span data-stu-id="f8619-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="f8619-114">Obtenga el estado actual de una característica o componente mediante una llamada a la función [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) o a la función [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="f8619-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="f8619-115">Cambiar el estado de la característica o componente con la función [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) o la función [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="f8619-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



