---
title: Settings. mediaAccessRights
description: La propiedad mediaAccessRights recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708801"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="c56e1-104">Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="c56e1-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="c56e1-105">La propiedad **mediaAccessRights** recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c56e1-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56e1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56e1-106">Syntax</span></span>

<span data-ttu-id="c56e1-107">Player. Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="c56e1-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="c56e1-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c56e1-108">Possible Values</span></span>

<span data-ttu-id="c56e1-109">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c56e1-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="c56e1-110">Value</span><span class="sxs-lookup"><span data-stu-id="c56e1-110">Value</span></span> | <span data-ttu-id="c56e1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c56e1-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="c56e1-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="c56e1-112">none</span></span>  | <span data-ttu-id="c56e1-113">Solo los derechos de acceso a elementos actuales.</span><span class="sxs-lookup"><span data-stu-id="c56e1-113">Current item access rights only.</span></span> |
| <span data-ttu-id="c56e1-114">leer</span><span class="sxs-lookup"><span data-stu-id="c56e1-114">read</span></span>  | <span data-ttu-id="c56e1-115">Solo derechos de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="c56e1-115">Read access rights only.</span></span>         |
| <span data-ttu-id="c56e1-116">full</span><span class="sxs-lookup"><span data-stu-id="c56e1-116">full</span></span>  | <span data-ttu-id="c56e1-117">Derechos de acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c56e1-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="c56e1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c56e1-118">Remarks</span></span>

<span data-ttu-id="c56e1-119">Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c56e1-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="c56e1-120">Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c56e1-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="c56e1-121">Para obtener derechos de acceso, la aplicación llama a la *configuración*. **requestMediaAccessRights**, pasando un parámetro que especifica el nivel de derechos de acceso deseado.</span><span class="sxs-lookup"><span data-stu-id="c56e1-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="c56e1-122">**Windows Media Player 10 Mobile**: esta propiedad siempre devuelve **Full**.</span><span class="sxs-lookup"><span data-stu-id="c56e1-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56e1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56e1-123">Requirements</span></span>



| <span data-ttu-id="c56e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56e1-124">Requirement</span></span> | <span data-ttu-id="c56e1-125">Value</span><span class="sxs-lookup"><span data-stu-id="c56e1-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c56e1-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c56e1-126">Version</span></span><br/> | <span data-ttu-id="c56e1-127">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="c56e1-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c56e1-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c56e1-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c56e1-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56e1-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56e1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56e1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56e1-131">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="c56e1-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="c56e1-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c56e1-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





