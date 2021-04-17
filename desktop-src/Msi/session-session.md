---
description: La propiedad Property del objeto de sesión es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal y como la mantiene el objeto de sesión.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propiedad Session. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681124"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="91355-103">Propiedad Session. Property</span><span class="sxs-lookup"><span data-stu-id="91355-103">Session.Property property</span></span>

<span data-ttu-id="91355-104">La propiedad **Property** del objeto de [**sesión**](session-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal como la mantiene el objeto de **sesión** en la tabla de propiedades en memoria, o bien, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="91355-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="91355-105">Se pueden proporcionar valores de cadena o enteros.</span><span class="sxs-lookup"><span data-stu-id="91355-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="91355-106">Una propiedad o una variable de entorno inexistente equivale a su valor null.</span><span class="sxs-lookup"><span data-stu-id="91355-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="91355-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="91355-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="91355-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91355-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="91355-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="91355-109">Property value</span></span>

<span data-ttu-id="91355-110">Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad o un nombre que no distingue entre mayúsculas y minúsculas de una variable de entorno con un signo de porcentaje (%).</span><span class="sxs-lookup"><span data-stu-id="91355-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="91355-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91355-111">Requirements</span></span>



| <span data-ttu-id="91355-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="91355-112">Requirement</span></span> | <span data-ttu-id="91355-113">Value</span><span class="sxs-lookup"><span data-stu-id="91355-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91355-114">Versión</span><span class="sxs-lookup"><span data-stu-id="91355-114">Version</span></span><br/> | <span data-ttu-id="91355-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="91355-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="91355-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="91355-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="91355-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="91355-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="91355-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91355-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="91355-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91355-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="91355-120">IID</span><span class="sxs-lookup"><span data-stu-id="91355-120">IID</span></span><br/>     | <span data-ttu-id="91355-121">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="91355-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




