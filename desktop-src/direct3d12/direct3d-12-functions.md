---
title: Funciones principales (gráficos de Direct3D 12)
description: Las siguientes funciones se declaran en d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: 99ec8516634a0a59262df9862e03732c9d6d579a
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "105704877"
---
# <a name="core-functions"></a><span data-ttu-id="325cb-103">Funciones principales</span><span class="sxs-lookup"><span data-stu-id="325cb-103">Core functions</span></span>

<span data-ttu-id="325cb-104">Las siguientes funciones se declaran en d3d12. h.</span><span class="sxs-lookup"><span data-stu-id="325cb-104">The following functions are declared in d3d12.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="325cb-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="325cb-105">In this section</span></span>

| <span data-ttu-id="325cb-106">Tema</span><span class="sxs-lookup"><span data-stu-id="325cb-106">Topic</span></span> | <span data-ttu-id="325cb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="325cb-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="325cb-108">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="325cb-108">**D3D12CreateDevice**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | <span data-ttu-id="325cb-109">Crea un dispositivo que representa el adaptador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="325cb-109">Creates a device that represents the display adapter.</span></span> |
| [<span data-ttu-id="325cb-110">**D3D12CreateRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="325cb-110">**D3D12CreateRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | <span data-ttu-id="325cb-111">Deserializa una firma raíz para que pueda determinar la definición de diseño ([**D3D12 \_ raíz de la \_ firma \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span><span class="sxs-lookup"><span data-stu-id="325cb-111">Deserializes a root signature so you can determine the layout definition ([**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)).</span></span> |
| [<span data-ttu-id="325cb-112">**D3D12CreateVersionedRootSignatureDeserializer**</span><span class="sxs-lookup"><span data-stu-id="325cb-112">**D3D12CreateVersionedRootSignatureDeserializer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | <span data-ttu-id="325cb-113">Genera una interfaz que puede devolver la estructura de datos deserializada a través de [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span><span class="sxs-lookup"><span data-stu-id="325cb-113">Generates an interface that can return the deserialized data structure, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).</span></span> |
| [<span data-ttu-id="325cb-114">**D3D12EnableExperimentalFeatures**</span><span class="sxs-lookup"><span data-stu-id="325cb-114">**D3D12EnableExperimentalFeatures**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | <span data-ttu-id="325cb-115">Habilita una lista de características experimentales.</span><span class="sxs-lookup"><span data-stu-id="325cb-115">Enables a list of experimental features.</span></span> |
| [<span data-ttu-id="325cb-116">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="325cb-116">**D3D12GetDebugInterface**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | <span data-ttu-id="325cb-117">Obtiene una interfaz de depuración.</span><span class="sxs-lookup"><span data-stu-id="325cb-117">Gets a debug interface.</span></span> |
| [<span data-ttu-id="325cb-118">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="325cb-118">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | <span data-ttu-id="325cb-119">Serializa la versión 1,0 de la firma raíz que se puede pasar a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="325cb-119">Serializes a root signature version 1.0 that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |
| [<span data-ttu-id="325cb-120">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="325cb-120">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | <span data-ttu-id="325cb-121">Serializa una firma raíz de cualquier versión que se pueda pasar a [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span><span class="sxs-lookup"><span data-stu-id="325cb-121">Serializes a root signature of any version that can be passed to [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).</span></span> |

## <a name="related-topics"></a><span data-ttu-id="325cb-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="325cb-122">Related topics</span></span>

* [<span data-ttu-id="325cb-123">Referencia principal</span><span class="sxs-lookup"><span data-stu-id="325cb-123">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="325cb-124">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="325cb-124">Direct3D 12 reference</span></span>](direct3d-12-reference.md)






