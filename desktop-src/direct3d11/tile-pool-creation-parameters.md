---
title: Parámetros de creación de grupos de iconos
description: Use los parámetros de esta sección para definir grupos de mosaicos a través de la API ID3D11Device CreateBuffer.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966887"
---
# <a name="tile-pool-creation-parameters"></a>Parámetros de creación de grupos de iconos

Use los parámetros de esta sección para definir grupos de mosaicos a través de la API [**ID3D11Device::CreateBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Tamaño**
</dt> <dd>

Tamaño de asignación, como un múltiplo de 64 KB. 0 es válido porque más adelante puede usar una operación [**ID3D11DeviceContext2::ResizeTilePool.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Marcas misc de recursos admitidas**
</dt> <dd>

GRUPO DE MOSAICOS MISC DE RECURSOS D3D11 (identifica el recurso como un grupo de \_ \_ \_ \_ mosaicos), RECURSO D3D11 \_ \_ MISC \_ SHARED, \_ SHARED \_ KEYEDMUTEX o \_ SHARED \_ NTHANDLE.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Uso de recursos admitido**
</dt> <dd>

SOLO EL VALOR PREDETERMINADO DE USO DE D3D11. \_ \_

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de recursos en mosaico](creating-tiled-resources.md)
</dt> </dl>

 

 




