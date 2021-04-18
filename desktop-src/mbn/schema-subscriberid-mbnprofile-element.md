---
description: Identifica el identificador único del perfil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: SubscriberID (MBNProfile), elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542182"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="d397f-103">SubscriberID (MBNProfile), elemento</span><span class="sxs-lookup"><span data-stu-id="d397f-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="d397f-104">El elemento **SubscriberID (MBNProfile)** identifica el identificador único del perfil.</span><span class="sxs-lookup"><span data-stu-id="d397f-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="d397f-105">En el caso de una red GSM, debe contener la IMSI (identidad del suscriptor móvil internacional) de la tarjeta SIM y los dispositivos CDMA deben contener el número mínimo de identificación móvil del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d397f-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="d397f-106">El elemento es una cadena numérica con una longitud máxima de 15 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d397f-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="d397f-107">El elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d397f-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="d397f-108">El elemento **SubscriberID** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d397f-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d397f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d397f-109">Requirements</span></span>



| <span data-ttu-id="d397f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d397f-110">Requirement</span></span> | <span data-ttu-id="d397f-111">Value</span><span class="sxs-lookup"><span data-stu-id="d397f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d397f-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d397f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d397f-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d397f-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d397f-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d397f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d397f-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d397f-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d397f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d397f-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d397f-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d397f-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d397f-118">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d397f-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d397f-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d397f-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d397f-120">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d397f-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




