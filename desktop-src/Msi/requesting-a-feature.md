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
# <a name="requesting-a-feature"></a><span data-ttu-id="2d12b-103">Solicitar una característica</span><span class="sxs-lookup"><span data-stu-id="2d12b-103">Requesting a Feature</span></span>

<span data-ttu-id="2d12b-104">Hay varias funciones a las que una aplicación debe llamar para solicitar características.</span><span class="sxs-lookup"><span data-stu-id="2d12b-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="2d12b-105">Antes de solicitar una característica, la aplicación debe asegurarse de que la característica está instalada.</span><span class="sxs-lookup"><span data-stu-id="2d12b-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="2d12b-106">Si la aplicación llama a [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) antes de que la aplicación tenga acceso a una característica, la aplicación puede usar la información devuelta para mantener las métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="2d12b-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="2d12b-107">**Para solicitar una característica**</span><span class="sxs-lookup"><span data-stu-id="2d12b-107">**To request a feature**</span></span>

1.  <span data-ttu-id="2d12b-108">Llame a la función [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) o [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) si quiere determinar la disponibilidad de una característica sin incrementar el recuento de uso.</span><span class="sxs-lookup"><span data-stu-id="2d12b-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="2d12b-109">Indique la intención de la aplicación de usar una característica mediante una llamada a la función [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="2d12b-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="2d12b-110">Determinar las ubicaciones de los archivos mediante una llamada a la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .</span><span class="sxs-lookup"><span data-stu-id="2d12b-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="2d12b-111">Configure la característica mediante una llamada a la función [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="2d12b-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="2d12b-112">Obtener métricas de uso que la aplicación puede usar mediante una llamada a la función [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .</span><span class="sxs-lookup"><span data-stu-id="2d12b-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="2d12b-113">En el diagrama siguiente se ilustra el modelo de solicitud de características.</span><span class="sxs-lookup"><span data-stu-id="2d12b-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="2d12b-114">modelo de solicitud de características.</span><span class="sxs-lookup"><span data-stu-id="2d12b-114">feature request model.</span></span> ](images/over2.png)

 

 



