---
description: Definir propiedades personalizadas.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definir propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697174"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="34956-103">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="34956-103">Defining Custom Properties</span></span>

<span data-ttu-id="34956-104">**Definir propiedades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="34956-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="34956-105">Si es necesario que el minicontrolador de adquisición de imágenes de Windows (WIA) defina las propiedades personalizadas, \_ se \_ debe usar la propiedad DEVPROP privada de WIA para las propiedades de los elementos raíz personalizados y la \_ \_ propiedad ITEMPROP privada de WIA para otras propiedades de elemento.</span><span class="sxs-lookup"><span data-stu-id="34956-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="34956-106">Estas constantes se definen en *wiadef. h*.</span><span class="sxs-lookup"><span data-stu-id="34956-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="34956-107">En el ejemplo de código siguiente se muestran definiciones de tres propiedades de elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="34956-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="34956-108">El identificador de propiedad de la primera propiedad de elemento raíz personalizado \_ , \_ prop \_ . raíz personalizada 1, se define en términos de \_ DEVPROP privado de WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="34956-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="34956-109">Los identificadores de propiedad para las propiedades adicionales de los elementos raíz se definen en términos de WIA \_ Private \_ DEVPROP + 1, WIA \_ Private \_ DEVPROP + 2, etc.</span><span class="sxs-lookup"><span data-stu-id="34956-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="34956-110">El patrón puede continuar si se necesitan propiedades adicionales del elemento raíz personalizado.</span><span class="sxs-lookup"><span data-stu-id="34956-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="34956-111">En el ejemplo siguiente se muestran definiciones de tres propiedades de elementos secundarios y identificadores de propiedad personalizados.</span><span class="sxs-lookup"><span data-stu-id="34956-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="34956-112">El identificador de propiedad de la primera propiedad de elemento secundario personalizada, CUSTOM \_ Child \_ prop \_ 1, se define en términos de \_ ITEMPROP privado de WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="34956-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="34956-113">Los identificadores de propiedad para las propiedades adicionales de los elementos secundarios se definen en términos de \_ ITEMPROPs privados de WIA \_ + 1, etc.</span><span class="sxs-lookup"><span data-stu-id="34956-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="34956-114">Como antes, el patrón puede continuar si se necesitan más de estas propiedades de elemento secundario personalizadas.</span><span class="sxs-lookup"><span data-stu-id="34956-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="34956-115">Las propiedades de WIA personalizadas deben tener nombres de propiedad personalizados que estén asociados a los identificadores de las propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="34956-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="34956-116">En el ejemplo de código siguiente se muestran definiciones de tres nombres de propiedad de elementos raíz personalizados.</span><span class="sxs-lookup"><span data-stu-id="34956-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="34956-117">(Estos nombres de propiedad se usan con los identificadores de propiedad personalizados que se crearon en un ejemplo anterior, donde el nombre de la propiedad personalizada contenía el personalizado \_ \_La Prop raíz \_ 1 \_ Str está asociada al identificador de la propiedad del elemento raíz personalizado \_ \_ prop \_ .</span><span class="sxs-lookup"><span data-stu-id="34956-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="34956-118">Los nombres de las propiedades de WIA *no* se localizan en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="34956-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="34956-119">Esto se debe a que las aplicaciones pueden leer las propiedades de WIA mediante el identificador de propiedad o el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="34956-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="34956-120">Si se usa el nombre, debe ser una constante, del mismo modo que el identificador de la propiedad es.</span><span class="sxs-lookup"><span data-stu-id="34956-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



