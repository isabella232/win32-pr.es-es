---
title: Settings. requestMediaAccessRights (método)
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | Settings. requestMediaAccessRights (método)
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- método requestMediaAccessRights de Windows Media Player
- método requestMediaAccessRights de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653572"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="c1aa4-107">Settings. requestMediaAccessRights (método)</span><span class="sxs-lookup"><span data-stu-id="c1aa4-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="c1aa4-108">El método **requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1aa4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1aa4-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="c1aa4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1aa4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1aa4-111">*acceso a* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c1aa4-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1aa4-112">**Cadena** que especifica el nivel de derechos de acceso deseado.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="c1aa4-113">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-113">Contains one of the following values.</span></span>



| <span data-ttu-id="c1aa4-114">String</span><span class="sxs-lookup"><span data-stu-id="c1aa4-114">String</span></span> | <span data-ttu-id="c1aa4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1aa4-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="c1aa4-116">ninguno</span><span class="sxs-lookup"><span data-stu-id="c1aa4-116">none</span></span>   | <span data-ttu-id="c1aa4-117">Solo los derechos de acceso a elementos actuales.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-117">Current item access rights only.</span></span> |
| <span data-ttu-id="c1aa4-118">leer</span><span class="sxs-lookup"><span data-stu-id="c1aa4-118">read</span></span>   | <span data-ttu-id="c1aa4-119">Solo derechos de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-119">Read access rights only.</span></span>         |
| <span data-ttu-id="c1aa4-120">full</span><span class="sxs-lookup"><span data-stu-id="c1aa4-120">full</span></span>   | <span data-ttu-id="c1aa4-121">Derechos de acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1aa4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1aa4-122">Return value</span></span>

<span data-ttu-id="c1aa4-123">Este método devuelve un valor **booleano** que indica si se concedieron los derechos de acceso solicitados.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1aa4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1aa4-124">Remarks</span></span>

<span data-ttu-id="c1aa4-125">Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="c1aa4-126">Al invocar este método, se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="c1aa4-127">Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="c1aa4-128">El nivel de derechos de acceso actual se puede recuperar mediante la *configuración*. **mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="c1aa4-129">**Windows Media Player 10 Mobile**: este método siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1aa4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1aa4-130">Requirements</span></span>



| <span data-ttu-id="c1aa4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1aa4-131">Requirement</span></span> | <span data-ttu-id="c1aa4-132">Value</span><span class="sxs-lookup"><span data-stu-id="c1aa4-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1aa4-133">Versión</span><span class="sxs-lookup"><span data-stu-id="c1aa4-133">Version</span></span><br/> | <span data-ttu-id="c1aa4-134">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="c1aa4-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c1aa4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1aa4-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1aa4-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa4-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1aa4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1aa4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aa4-138">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="c1aa4-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="c1aa4-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c1aa4-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





