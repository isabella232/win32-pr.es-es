---
title: Función MrmDestroyIndexerAndMessages (MrmResourceIndexer. h)
description: Libera los recursos de la máquina asociados a un indizador de recursos.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menús de la función MrmDestroyIndexerAndMessages y otros recursos
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079745"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="c7cbf-104">MrmDestroyIndexerAndMessages función)</span><span class="sxs-lookup"><span data-stu-id="c7cbf-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="c7cbf-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c7cbf-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c7cbf-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c7cbf-107">Libera los recursos de la máquina asociados a un indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="c7cbf-108">Destruye el identificador, libera el indizador y elimina todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="c7cbf-109">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="c7cbf-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7cbf-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7cbf-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="c7cbf-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7cbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7cbf-112">*indexador* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7cbf-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cbf-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cbf-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="c7cbf-114">Identificador que identifica el indizador de recursos que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7cbf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7cbf-115">Return value</span></span>

<span data-ttu-id="c7cbf-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c7cbf-116">Type: **HRESULT**</span></span>

<span data-ttu-id="c7cbf-117">Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="c7cbf-118">Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c7cbf-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7cbf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7cbf-119">Requirements</span></span>



| <span data-ttu-id="c7cbf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7cbf-120">Requirement</span></span> | <span data-ttu-id="c7cbf-121">Value</span><span class="sxs-lookup"><span data-stu-id="c7cbf-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cbf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7cbf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7cbf-123">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7cbf-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c7cbf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7cbf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7cbf-125">Solo aplicaciones de escritorio de Windows Server \[\]</span><span class="sxs-lookup"><span data-stu-id="c7cbf-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7cbf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7cbf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7cbf-127"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7cbf-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="c7cbf-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7cbf-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7cbf-129"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7cbf-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="c7cbf-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7cbf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7cbf-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7cbf-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c7cbf-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7cbf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7cbf-133">API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados</span><span class="sxs-lookup"><span data-stu-id="c7cbf-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

