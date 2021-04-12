---
description: Especifica si las redes denegadas aparecen en el Asistente para conectarse a una red.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Elemento showDeniedNetwork (Indicadores_globales)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543758"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="a6aef-103">Elemento showDeniedNetwork (Indicadores_globales)</span><span class="sxs-lookup"><span data-stu-id="a6aef-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="a6aef-104">El elemento **showDeniedNetwork** (indicadores_globales) especifica si las redes denegadas aparecen en el Asistente para **conectarse a una red** .</span><span class="sxs-lookup"><span data-stu-id="a6aef-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="a6aef-105">La Directiva de grupo o la configuración de usuario pueden denegar las redes.</span><span class="sxs-lookup"><span data-stu-id="a6aef-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="a6aef-106">Cuando **showDeniedNetwork** tiene un valor true, las redes denegadas aparecen en el Asistente para **conectarse a una red** ; de lo contrario, las redes denegadas no aparecen en el asistente.</span><span class="sxs-lookup"><span data-stu-id="a6aef-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="a6aef-107">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6aef-107">This element is mandatory.</span></span> <span data-ttu-id="a6aef-108">Cuando el servicio de configuración automática crea un perfil, este elemento toma el valor predeterminado de FALSE.</span><span class="sxs-lookup"><span data-stu-id="a6aef-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="a6aef-109">El elemento **showDeniedNetwork** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a6aef-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6aef-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6aef-110">Requirements</span></span>



| <span data-ttu-id="a6aef-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6aef-111">Requirement</span></span> | <span data-ttu-id="a6aef-112">Value</span><span class="sxs-lookup"><span data-stu-id="a6aef-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6aef-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6aef-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a6aef-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6aef-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a6aef-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6aef-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a6aef-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6aef-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6aef-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6aef-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6aef-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a6aef-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a6aef-119">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="a6aef-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="a6aef-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6aef-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a6aef-121">**Indicadores_globales (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="a6aef-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




