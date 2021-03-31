---
title: Atributos de valor único frente a varios valores
description: Los atributos que pueden existir en un directorio se definen normalmente en el esquema para el directorio.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI en comparación con los atributos de valor múltiple
- atributos ADSI, atributos de valor único frente a varios valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075059"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="a6aee-105">Atributos de valor único frente a varios valores</span><span class="sxs-lookup"><span data-stu-id="a6aee-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="a6aee-106">Los atributos que pueden existir en un directorio se definen normalmente en el esquema para el directorio.</span><span class="sxs-lookup"><span data-stu-id="a6aee-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="a6aee-107">La definición de esquema de un atributo especifica varias características del atributo, como el tipo de datos y si una instancia del atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="a6aee-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="a6aee-108">Una instancia de un atributo de un solo valor puede contener un valor único.</span><span class="sxs-lookup"><span data-stu-id="a6aee-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="a6aee-109">Una instancia de un atributo multivalor puede contener un solo valor o varios valores.</span><span class="sxs-lookup"><span data-stu-id="a6aee-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="a6aee-110">Active Directory no crea atributos con valores vacíos, o bien el atributo contiene un valor válido o no existe en el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6aee-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="a6aee-111">En Active Directory y la mayoría de los demás servidores LDAP, el orden de los valores de un atributo con varios valores es indefinido.</span><span class="sxs-lookup"><span data-stu-id="a6aee-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="a6aee-112">Además, cada valor de un atributo con varios valores debe ser único.</span><span class="sxs-lookup"><span data-stu-id="a6aee-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="a6aee-113">Normalmente, ADSI carga los datos del esquema si el directorio admite un esquema, como hace Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a6aee-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="a6aee-114">Dado que ADSI conoce la sintaxis de los atributos en el esquema, no es necesario especificar el tipo de atributo cuando se tiene acceso a él.</span><span class="sxs-lookup"><span data-stu-id="a6aee-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="a6aee-115">ADSI calcula las referencias de los valores de atributo en el tipo de datos adecuado, tal y como se define en el esquema.</span><span class="sxs-lookup"><span data-stu-id="a6aee-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="a6aee-116">Si el directorio no tiene ningún esquema, proporcione el tipo de datos al tener acceso a un atributo.</span><span class="sxs-lookup"><span data-stu-id="a6aee-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="a6aee-117">Active Directory, Exchange, Windows NT 4,0 y el servidor de sitio tienen un esquema.</span><span class="sxs-lookup"><span data-stu-id="a6aee-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="a6aee-118">Además, Active Directory tiene un esquema extensible.</span><span class="sxs-lookup"><span data-stu-id="a6aee-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




