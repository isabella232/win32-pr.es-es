---
description: Determina si una configuración regional especificada por nombre se instala o se admite en el sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Función RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907892"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="8d17d-103">RtlIsValidLocaleName función)</span><span class="sxs-lookup"><span data-stu-id="8d17d-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="8d17d-104">Determina si una configuración regional especificada por nombre se instala o se admite en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8d17d-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="8d17d-105">Esta función solo está disponible para su uso en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d17d-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="8d17d-106">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8d17d-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8d17d-107">Las aplicaciones deben usar [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="8d17d-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8d17d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d17d-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8d17d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d17d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d17d-110">*LocaleName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d17d-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d17d-111">[Nombre de la configuración regional](locale-names.md) que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="8d17d-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="8d17d-112">Este parámetro puede especificar el nombre de una [configuración regional personalizada](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="8d17d-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d17d-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8d17d-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d17d-114">Marcas que indican si las configuraciones regionales neutras se consideran válidas.</span><span class="sxs-lookup"><span data-stu-id="8d17d-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="8d17d-115">Actualmente, la única marca definida es [ \_ permitir la \_ configuración regional](locale-allow-neutral.md).</span><span class="sxs-lookup"><span data-stu-id="8d17d-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="8d17d-116">El valor predeterminado es que no son.</span><span class="sxs-lookup"><span data-stu-id="8d17d-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d17d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d17d-117">Return value</span></span>

<span data-ttu-id="8d17d-118">Devuelve un valor distinto de cero si es correcto o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8d17d-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d17d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d17d-119">Remarks</span></span>

<span data-ttu-id="8d17d-120">Esta función es similar a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="8d17d-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="8d17d-121">La única diferencia es que si se establece la configuración regional \_ Allow \_ neutral, **RtlIsValidLocaleName** devuelve **true** para un nombre que se corresponde con una configuración regional neutra (como "en"), mientras que [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) solo devuelve **true** para una configuración regional concreta (como "en-US").</span><span class="sxs-lookup"><span data-stu-id="8d17d-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="8d17d-122">Las configuraciones regionales neutras se utilizan como parte de la estrategia de carga de recursos en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8d17d-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="8d17d-123">Solo una pequeña clase de aplicaciones muy especializadas usa **RtlIsValidLocaleName** y establece la configuración regional para \_ que \_ sea neutra, ya que las configuraciones regionales neutras son de uso muy limitado.</span><span class="sxs-lookup"><span data-stu-id="8d17d-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="8d17d-124">Ninguna de las funciones descritas en [llamada a las funciones de "nombre de configuración regional"](calling-the--locale-name--functions.md) acepta configuraciones regionales neutras como entradas.</span><span class="sxs-lookup"><span data-stu-id="8d17d-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d17d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d17d-125">Requirements</span></span>



| <span data-ttu-id="8d17d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d17d-126">Requirement</span></span> | <span data-ttu-id="8d17d-127">Value</span><span class="sxs-lookup"><span data-stu-id="8d17d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d17d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d17d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d17d-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8d17d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8d17d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d17d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d17d-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d17d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d17d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d17d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d17d-133"><dt>Ntrtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d17d-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="8d17d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d17d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d17d-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d17d-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d17d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d17d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d17d-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d17d-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d17d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d17d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d17d-139">Compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="8d17d-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="8d17d-140">Funciones de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="8d17d-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="8d17d-141">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="8d17d-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




