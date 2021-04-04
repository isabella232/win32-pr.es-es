---
description: Especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154577"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="9d84d-103">Elemento userBasedVirtualLan (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="9d84d-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="9d84d-104">El elemento userBasedVirtualLan (singleSignOn) especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="9d84d-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="9d84d-105">Algunos dispositivos del servidor de acceso a la red (NAS) cambian la VLAN después de que un usuario se autentique.</span><span class="sxs-lookup"><span data-stu-id="9d84d-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="9d84d-106">Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique.</span><span class="sxs-lookup"><span data-stu-id="9d84d-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="9d84d-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9d84d-107">This element is optional.</span></span> <span data-ttu-id="9d84d-108">Cuando userBasedVirtualLan no se especifica en un perfil, se usa un valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="9d84d-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="9d84d-109">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento se omitirá si está presente en un perfil.</span><span class="sxs-lookup"><span data-stu-id="9d84d-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="9d84d-110">El elemento **userBasedVirtualLan** se define mediante el elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9d84d-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d84d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d84d-111">Remarks</span></span>

<span data-ttu-id="9d84d-112">Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter**</span><span class="sxs-lookup"><span data-stu-id="9d84d-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="9d84d-113">Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9d84d-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d84d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d84d-114">Requirements</span></span>



| <span data-ttu-id="9d84d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d84d-115">Requirement</span></span> | <span data-ttu-id="9d84d-116">Value</span><span class="sxs-lookup"><span data-stu-id="9d84d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d84d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d84d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d84d-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9d84d-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d84d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d84d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d84d-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d84d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d84d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d84d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d84d-122">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="9d84d-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9d84d-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="9d84d-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="9d84d-124">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="9d84d-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9d84d-125">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="9d84d-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
