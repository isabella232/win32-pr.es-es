---
title: Funciones principales (gráficos de Direct3D 12)
description: Las siguientes funciones se declaran en d3d12.h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: e38145bc4aef4c07ba00de4185fc97ad449f4f2c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881790"
---
# <a name="core-functions"></a>Funciones principales

Las siguientes funciones se declaran en d3d12.h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | Crea un dispositivo que representa el adaptador de pantalla. |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | Deserializa una firma raíz para que pueda determinar la definición de diseño ([**D3D12 \_ ROOT \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)). |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | Genera una interfaz que puede devolver la estructura de datos deserialización, a través de [**GetUnconvertedRootSignatureDesc.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | Habilita una lista de características experimentales. |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | Obtiene una interfaz de depuración. |
| [**D3D12GetInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Selecciona una versión del SDK en tiempo de ejecución cuando el sistema está Windows modo de desarrollador. |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | Serializa una firma raíz versión 1.0 que se puede pasar a [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Serializa una firma raíz de cualquier versión que se pueda pasar a [**ID3D12Device::CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
