---
title: Asignar nombres a atributos y clases
description: En este tema se incluyen instrucciones para asignar nombres a los atributos y las clases.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Asignar nombres a atributos y clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "105656437"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="916fe-104">Asignar nombres a atributos y clases</span><span class="sxs-lookup"><span data-stu-id="916fe-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="916fe-105">En este tema se incluyen instrucciones para asignar nombres a los atributos y las clases.</span><span class="sxs-lookup"><span data-stu-id="916fe-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="916fe-106">Para crear una nueva clase o atributo, cumpla las siguientes reglas de nomenclatura:</span><span class="sxs-lookup"><span data-stu-id="916fe-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="916fe-107">Use el mismo nombre para las propiedades **CN** y **lDAPDisplayName** de un nuevo objeto **attributeSchema** o **ClassSchema** .</span><span class="sxs-lookup"><span data-stu-id="916fe-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="916fe-108">Identifique la empresa con un prefijo en minúsculas en la primera sección del nombre.</span><span class="sxs-lookup"><span data-stu-id="916fe-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="916fe-109">Este prefijo puede ser un nombre DNS, un acrónimo u otra cadena que identifique de forma única a la empresa.</span><span class="sxs-lookup"><span data-stu-id="916fe-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="916fe-110">El prefijo garantiza que todos los atributos y las clases de una empresa específica se muestran de manera consecutiva al examinar el esquema.</span><span class="sxs-lookup"><span data-stu-id="916fe-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="916fe-111">Si está desarrollando una extensión de esquema como proveedor de software independiente, agregue una abreviatura del nombre de producto del prefijo.</span><span class="sxs-lookup"><span data-stu-id="916fe-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="916fe-112">Esto agrega distinción entre varios productos que contienen extensiones de esquema LDAP.</span><span class="sxs-lookup"><span data-stu-id="916fe-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="916fe-113">Use un guión como el carácter siguiente después del prefijo.</span><span class="sxs-lookup"><span data-stu-id="916fe-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="916fe-114">Especifique un nombre de clase o atributo que sea único dentro de los atributos de la compañía después del guión.</span><span class="sxs-lookup"><span data-stu-id="916fe-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="916fe-115">Esta parte de Common-Name debe ser descriptiva.</span><span class="sxs-lookup"><span data-stu-id="916fe-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="916fe-116">No utilice nombres de illogical que no tengan sentido para los desarrolladores y visores del esquema.</span><span class="sxs-lookup"><span data-stu-id="916fe-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="916fe-117">Por ejemplo, si la compañía ficticia Fabrikam amplió el esquema agregando un atributo para almacenar un identificador de correo de voz, el **CN** y el **lDAPDisplayName** del nuevo atributo podrían ser "fabrikam-VoiceMailID".</span><span class="sxs-lookup"><span data-stu-id="916fe-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="916fe-118">Si no se especifica el **lDAPDisplayName** de un atributo o una clase, el sistema utiliza el **CN** para generar uno.</span><span class="sxs-lookup"><span data-stu-id="916fe-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="916fe-119">Sin embargo, el algoritmo del sistema para generar el nombre puede dar lugar a conflictos de nombres o nombres difíciles de leer.</span><span class="sxs-lookup"><span data-stu-id="916fe-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="916fe-120">Para evitar estos problemas, se recomienda especificar explícitamente un **lDAPDisplayName** para todos los atributos y clases.</span><span class="sxs-lookup"><span data-stu-id="916fe-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="916fe-121">Para fines de desarrollo y pruebas, puede ser conveniente anexar un sufijo de versión a los **CN** y **lDAPDisplayName**, por ejemplo, "fabrikam-VoiceMailID-001".</span><span class="sxs-lookup"><span data-stu-id="916fe-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="916fe-122">En un entorno de desarrollo y pruebas distribuido, un sufijo de versión permite a los desarrolladores ejecutar varias versiones de su software simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="916fe-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="916fe-123">Una vez completadas las pruebas, cambie el nombre del atributo o de la clase para quitar el sufijo.</span><span class="sxs-lookup"><span data-stu-id="916fe-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="916fe-124">No es posible eliminar las versiones inactivas de las extensiones de esquema, pero es posible deshabilitarlas y cambiarlas por nombres más claros.</span><span class="sxs-lookup"><span data-stu-id="916fe-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="916fe-125">Para obtener más información, vea [deshabilitar clases y atributos existentes](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="916fe-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




