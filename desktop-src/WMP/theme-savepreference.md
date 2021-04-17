---
title: THEME. savePreference
description: El método savePreference guarda una preferencia en el registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- Media Player de Windows de THEME. savePreference
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709084"
---
# <a name="themesavepreference"></a><span data-ttu-id="b5cb8-104">THEME. savePreference</span><span class="sxs-lookup"><span data-stu-id="b5cb8-104">THEME.savePreference</span></span>

<span data-ttu-id="b5cb8-105">El método **savePreference** guarda una preferencia en el registro.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="b5cb8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5cb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cb8-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="b5cb8-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="b5cb8-108">**Cadena** que especifica la clave del valor de preferencia que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="b5cb8-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*El valorque*</span><span class="sxs-lookup"><span data-stu-id="b5cb8-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="b5cb8-110">**Cadena** que especifica el valor que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cb8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5cb8-111">Return Value</span></span>

<span data-ttu-id="b5cb8-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cb8-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5cb8-113">Remarks</span></span>

<span data-ttu-id="b5cb8-114">Una preferencia es un par clave-valor que se puede almacenar en el registro para conservar información sobre el estado de Windows Media Player entre ejecuciones.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="b5cb8-115">Esta característica se puede usar, por ejemplo, para guardar la configuración de personalización para que no sea necesario volver a escribirla cada vez que se inicie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="b5cb8-116">Las preferencias no se cifran y, por lo tanto, no son un método seguro para conservar los datos.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="b5cb8-117">No utilice preferencias para almacenar datos privados.</span><span class="sxs-lookup"><span data-stu-id="b5cb8-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="b5cb8-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b5cb8-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="b5cb8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5cb8-119">Requirements</span></span>



| <span data-ttu-id="b5cb8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cb8-120">Requirement</span></span> | <span data-ttu-id="b5cb8-121">Value</span><span class="sxs-lookup"><span data-stu-id="b5cb8-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b5cb8-122">Versión</span><span class="sxs-lookup"><span data-stu-id="b5cb8-122">Version</span></span><br/> | <span data-ttu-id="b5cb8-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b5cb8-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5cb8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5cb8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cb8-125">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="b5cb8-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="b5cb8-126">**THEME. loadPreference**</span><span class="sxs-lookup"><span data-stu-id="b5cb8-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





