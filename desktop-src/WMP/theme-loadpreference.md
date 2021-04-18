---
title: THEME. loadPreference
description: El método loadPreference carga una preferencia del registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Media Player de Windows de THEME. loadPreference
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681274"
---
# <a name="themeloadpreference"></a><span data-ttu-id="da63f-104">THEME. loadPreference</span><span class="sxs-lookup"><span data-stu-id="da63f-104">THEME.loadPreference</span></span>

<span data-ttu-id="da63f-105">El método **loadPreference** carga una preferencia del registro.</span><span class="sxs-lookup"><span data-stu-id="da63f-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="da63f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da63f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da63f-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="da63f-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="da63f-108">**Cadena** que especifica la clave del valor de preferencia que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="da63f-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da63f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da63f-109">Return Value</span></span>

<span data-ttu-id="da63f-110">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="da63f-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da63f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da63f-111">Remarks</span></span>

<span data-ttu-id="da63f-112">Una preferencia es un par clave-valor que se puede almacenar en el registro para conservar información sobre el estado de la Media Player de Windows entre ejecuciones.</span><span class="sxs-lookup"><span data-stu-id="da63f-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="da63f-113">Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización para que no sea necesario volver a escribirla cada vez que se inicie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="da63f-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="da63f-114">Las preferencias no se cifran y, por lo tanto, no son un método seguro para conservar los datos.</span><span class="sxs-lookup"><span data-stu-id="da63f-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="da63f-115">No utilice preferencias para almacenar datos privados.</span><span class="sxs-lookup"><span data-stu-id="da63f-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="da63f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da63f-116">Requirements</span></span>



| <span data-ttu-id="da63f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="da63f-117">Requirement</span></span> | <span data-ttu-id="da63f-118">Value</span><span class="sxs-lookup"><span data-stu-id="da63f-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="da63f-119">Versión</span><span class="sxs-lookup"><span data-stu-id="da63f-119">Version</span></span><br/> | <span data-ttu-id="da63f-120">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="da63f-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da63f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="da63f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da63f-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="da63f-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="da63f-123">**THEME. savePreference**</span><span class="sxs-lookup"><span data-stu-id="da63f-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





