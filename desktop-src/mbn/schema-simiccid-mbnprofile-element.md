---
description: Identifica el número de identificación de SIM para dispositivos GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Elemento SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666486"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="ce94e-103">Elemento SimIccID (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="ce94e-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="ce94e-104">El elemento **SimIccID (MBNProfile)** identifica el número de identificación de SIM para dispositivos GSM.</span><span class="sxs-lookup"><span data-stu-id="ce94e-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="ce94e-105">Este elemento es opcional y lo establece el servicio de banda ancha móvil para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ce94e-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="ce94e-106">Una aplicación no debe establecer este campo al crear o actualizar un perfil.</span><span class="sxs-lookup"><span data-stu-id="ce94e-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="ce94e-107">El elemento **SimIccID** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce94e-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce94e-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce94e-108">Requirements</span></span>



| <span data-ttu-id="ce94e-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce94e-109">Requirement</span></span> | <span data-ttu-id="ce94e-110">Value</span><span class="sxs-lookup"><span data-stu-id="ce94e-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ce94e-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce94e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ce94e-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce94e-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ce94e-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce94e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ce94e-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ce94e-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ce94e-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce94e-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce94e-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ce94e-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ce94e-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="ce94e-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="ce94e-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ce94e-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ce94e-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="ce94e-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




