---
description: Esta función toma el atributo Origin si está presente desde el token de origen y lo establece en un duplicado del token que hereda, y devuelve el token duplicado.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686674"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="ccbc1-103">srpInheritOriginClaim función)</span><span class="sxs-lookup"><span data-stu-id="ccbc1-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="ccbc1-104">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ccbc1-105">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ccbc1-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ccbc1-106">Esta función toma el atributo Origin si está presente desde el token de origen y lo establece en un duplicado del token que hereda, y devuelve el token duplicado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="ccbc1-107">Después, el autor de la llamada puede suplantar el token devuelto.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="ccbc1-108">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-108">This function has no associated import library.</span></span> <span data-ttu-id="ccbc1-109">Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a srpapi.dll.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccbc1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccbc1-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="ccbc1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccbc1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccbc1-112">*OriginToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccbc1-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbc1-113">Identificador del token que está duplicado y recibe el atributo de origen heredado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="ccbc1-114">Este identificador debe abrirse con el derecho de acceso de TOKEN \_ duplicado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="ccbc1-115">*InheritingToken* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccbc1-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccbc1-116">Identificador del token que está duplicado y recibe el atributo de origen heredado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="ccbc1-117">Este identificador debe abrirse con el derecho de acceso de TOKEN \_ duplicado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="ccbc1-118">*ResultToken*</span><span class="sxs-lookup"><span data-stu-id="ccbc1-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="ccbc1-119">Si se ejecuta correctamente, recibe el token duplicado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="ccbc1-120">El autor de la llamada puede suplantarlo para realizar operaciones con el atributo de origen heredado.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="ccbc1-121">El autor de la llamada toma la propiedad de este identificador y debe cerrarlo.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccbc1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccbc1-122">Return value</span></span>

<span data-ttu-id="ccbc1-123">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ccbc1-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ccbc1-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccbc1-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbc1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccbc1-125">Requirements</span></span>



| <span data-ttu-id="ccbc1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccbc1-126">Requirement</span></span> | <span data-ttu-id="ccbc1-127">Value</span><span class="sxs-lookup"><span data-stu-id="ccbc1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbc1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccbc1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ccbc1-129">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccbc1-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccbc1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccbc1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ccbc1-131">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccbc1-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccbc1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ccbc1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccbc1-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccbc1-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

