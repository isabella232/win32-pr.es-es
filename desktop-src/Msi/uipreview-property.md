---
description: La propiedad Property del objeto UIPreview es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, o bien, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Propiedad UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679555"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="7fbc9-103">Propiedad UIPreview. Property</span><span class="sxs-lookup"><span data-stu-id="7fbc9-103">UIPreview.Property property</span></span>

<span data-ttu-id="7fbc9-104">La propiedad **Property** del objeto [**UIPreview**](uipreview-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, o bien, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="7fbc9-105">Esto se expone para permitir la presentación adecuada de cuadros de diálogo que dependen de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="7fbc9-106">Se pueden proporcionar valores de cadena o enteros.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="7fbc9-107">Una propiedad o una variable de entorno inexistente equivale a su valor null.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="7fbc9-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbc9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fbc9-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="7fbc9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7fbc9-110">Property value</span></span>

<span data-ttu-id="7fbc9-111">Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad o un nombre que no distingue entre mayúsculas y minúsculas de una variable de entorno con un signo de porcentaje (%).</span><span class="sxs-lookup"><span data-stu-id="7fbc9-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbc9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbc9-112">Requirements</span></span>



| <span data-ttu-id="7fbc9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbc9-113">Requirement</span></span> | <span data-ttu-id="7fbc9-114">Value</span><span class="sxs-lookup"><span data-stu-id="7fbc9-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc9-115">Versión</span><span class="sxs-lookup"><span data-stu-id="7fbc9-115">Version</span></span><br/> | <span data-ttu-id="7fbc9-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7fbc9-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7fbc9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7fbc9-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fbc9-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7fbc9-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fbc9-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="7fbc9-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbc9-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7fbc9-121">IID</span><span class="sxs-lookup"><span data-stu-id="7fbc9-121">IID</span></span><br/>     | <span data-ttu-id="7fbc9-122">IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7fbc9-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




