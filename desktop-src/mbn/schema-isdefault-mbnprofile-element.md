---
description: Especifica si este es el perfil predeterminado para el dispositivo.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Elemento IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497374"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="f01d0-103">Elemento IsDefault (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="f01d0-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="f01d0-104">El elemento **IsDefault (MBNProfile)** especifica si este es el perfil predeterminado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f01d0-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="f01d0-105">Este es un elemento opcional y, si no se especifica, el perfil no se establecerá como el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f01d0-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="f01d0-106">El servicio de banda ancha móvil usa el perfil predeterminado para los siguientes fines</span><span class="sxs-lookup"><span data-stu-id="f01d0-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="f01d0-107">El servicio de banda ancha móvil usa la configuración de conexión del perfil predeterminado al realizar conexiones de red automáticas.</span><span class="sxs-lookup"><span data-stu-id="f01d0-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="f01d0-108">Esta configuración incluye el nombre del punto de acceso, el nombre de usuario, la contraseña, etc.</span><span class="sxs-lookup"><span data-stu-id="f01d0-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="f01d0-109">La Directiva de conexión automática para un dispositivo de banda ancha móvil se toma del perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f01d0-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="f01d0-110">La interfaz de usuario de conexión de red del sistema operativo también usa datos de conexión del perfil predeterminado para las operaciones de conexión.</span><span class="sxs-lookup"><span data-stu-id="f01d0-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="f01d0-111">Los proveedores de servicios móviles pueden proporcionar los detalles de conexión en un perfil y configurarlos como perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f01d0-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="f01d0-112">El servicio de banda ancha móvil usará esta configuración de conexión sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="f01d0-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="f01d0-113">El elemento **IsDefault** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f01d0-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01d0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f01d0-114">Requirements</span></span>



| <span data-ttu-id="f01d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01d0-115">Requirement</span></span> | <span data-ttu-id="f01d0-116">Value</span><span class="sxs-lookup"><span data-stu-id="f01d0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f01d0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f01d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f01d0-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f01d0-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f01d0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f01d0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f01d0-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f01d0-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f01d0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f01d0-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="f01d0-122">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="f01d0-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f01d0-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="f01d0-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="f01d0-124">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="f01d0-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f01d0-125">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="f01d0-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




