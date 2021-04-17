---
title: Función MrmFreeMemory (MrmResourceIndexer. h)
description: Libera memoria asignada por MrmCreateConfigInMemory, MrmCreateResourceFileInMemory, MrmDumpPriFileInMemory y MrmDumpPriDataInMemory.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Menús de la función MrmFreeMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666053"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="b4504-104">MrmFreeMemory función)</span><span class="sxs-lookup"><span data-stu-id="b4504-104">MrmFreeMemory function</span></span>

<span data-ttu-id="b4504-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b4504-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b4504-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b4504-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b4504-107">Libera memoria asignada por [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)y [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4504-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="b4504-108">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b4504-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4504-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4504-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="b4504-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4504-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4504-111">*datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b4504-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4504-112">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="b4504-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="b4504-113">Puntero a la memoria asignada y devuelta por [_ *MrmCreateConfigInMemory* \*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4504-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4504-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4504-114">Return value</span></span>

<span data-ttu-id="b4504-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b4504-115">Type: **HRESULT**</span></span>

<span data-ttu-id="b4504-116">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="b4504-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="b4504-117">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="b4504-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4504-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4504-118">Requirements</span></span>



| <span data-ttu-id="b4504-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4504-119">Requirement</span></span> | <span data-ttu-id="b4504-120">Value</span><span class="sxs-lookup"><span data-stu-id="b4504-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4504-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4504-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4504-122">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4504-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b4504-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4504-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4504-124">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="b4504-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4504-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4504-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4504-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4504-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="b4504-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4504-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4504-128"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4504-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="b4504-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4504-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4504-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4504-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b4504-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4504-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4504-132">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="b4504-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

