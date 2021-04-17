---
title: Username (elemento) (TLS)
description: Obtenga información sobre el elemento username. Este elemento captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Username (elemento) EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705027"
---
# <a name="username-element-tls"></a><span data-ttu-id="631ae-105">Username (elemento) (TLS)</span><span class="sxs-lookup"><span data-stu-id="631ae-105">Username element (TLS)</span></span>

<span data-ttu-id="631ae-106">El elemento **username** captura el nombre de usuario que se va a enviar en la EAP-Identity respuesta.</span><span class="sxs-lookup"><span data-stu-id="631ae-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="631ae-107">Si falta el elemento **username** , EAP-TLS usa el nombre del certificado al que se hace referencia en el elemento [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="631ae-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="631ae-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="631ae-108">Requirements</span></span>



| <span data-ttu-id="631ae-109">Role</span><span class="sxs-lookup"><span data-stu-id="631ae-109">Role</span></span> | <span data-ttu-id="631ae-110">Versiones mínimas admitidas del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="631ae-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="631ae-111">Remoto</span><span class="sxs-lookup"><span data-stu-id="631ae-111">Client</span></span><br/> | <span data-ttu-id="631ae-112">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="631ae-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="631ae-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="631ae-113">Server</span></span><br/> | <span data-ttu-id="631ae-114">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="631ae-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="631ae-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="631ae-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631ae-116">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="631ae-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="631ae-117">Esquema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="631ae-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





