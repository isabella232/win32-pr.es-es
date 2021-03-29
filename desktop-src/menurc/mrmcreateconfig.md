---
title: Función MrmCreateConfig (MrmResourceIndexer. h)
description: Crea un nuevo archivo de configuración de PRI inicializado que define los valores predeterminados del calificador que especifique. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Menús de la función MrmCreateConfig y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666057"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="c085d-105">MrmCreateConfig función)</span><span class="sxs-lookup"><span data-stu-id="c085d-105">MrmCreateConfig function</span></span>

<span data-ttu-id="c085d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c085d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c085d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c085d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c085d-108">Crea un nuevo archivo de configuración de PRI inicializado que define los valores predeterminados del calificador que especifique.</span><span class="sxs-lookup"><span data-stu-id="c085d-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="c085d-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="c085d-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="c085d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c085d-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="c085d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c085d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c085d-112">*platformVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c085d-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c085d-113">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="c085d-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="c085d-114">Versión de la plataforma (*targetOsVersion*) que se va a usar para el archivo de configuración generado.</span><span class="sxs-lookup"><span data-stu-id="c085d-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="c085d-115">*defaultQualifiers* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c085d-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c085d-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c085d-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="c085d-117">Una lista de calificadores de recursos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c085d-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="c085d-118">Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"</span><span class="sxs-lookup"><span data-stu-id="c085d-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="c085d-119">*outputXmlFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c085d-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c085d-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c085d-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="c085d-121">Ruta de acceso del archivo de configuración que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c085d-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c085d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c085d-122">Return value</span></span>

<span data-ttu-id="c085d-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c085d-123">Type: **HRESULT**</span></span>

<span data-ttu-id="c085d-124">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="c085d-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="c085d-125">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c085d-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c085d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c085d-126">Requirements</span></span>



| <span data-ttu-id="c085d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c085d-127">Requirement</span></span> | <span data-ttu-id="c085d-128">Value</span><span class="sxs-lookup"><span data-stu-id="c085d-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c085d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c085d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c085d-130">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="c085d-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c085d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c085d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c085d-132">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="c085d-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c085d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c085d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c085d-134"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c085d-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="c085d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c085d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c085d-136"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c085d-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="c085d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c085d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c085d-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c085d-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c085d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c085d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c085d-140">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="c085d-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

