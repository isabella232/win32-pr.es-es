---
title: Cómo inicializar una textura mediante programación
description: En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas creadas con distintos tipos de usos.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b7d34e7e85fd647a6f45c93d61b3330825261f59d87b9c13a95547e742e365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530567"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Cómo: Inicializar una textura mediante programación

Puede inicializar una textura durante la creación del objeto o rellenar el objeto mediante programación después de crearlo. En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas creadas con distintos tipos de usos. En este ejemplo se supone que ya sabe cómo [crear una textura](overviews-direct3d-11-resources-textures-create.md).

-   [Uso predeterminado](#default-usage)
-   [Uso dinámico](#dynamic-usage)
-   [Uso de almacenamiento provisional](#staging-usage)
-   [Temas relacionados](#related-topics)

## <a name="default-usage"></a>Uso predeterminado

El tipo de uso más común es el uso predeterminado. Para rellenar una textura predeterminada (una creada con **D3D11 \_ USAGE \_ DEFAULT),** puede:

-   Llame [**a ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inicialice *pInitialData* para que apunte a los datos proporcionados desde una aplicación.

    o

-   Después de llamar a [**ID3D11Device::CreateTexture2D,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para rellenar la textura predeterminada con datos de un puntero proporcionado por la aplicación.

## <a name="dynamic-usage"></a>Uso dinámico

Para rellenar una textura dinámica (una creada con **D3D11 \_ USAGE \_ DYNAMIC):**

1.  Obtenga un puntero a la memoria de textura pasando **D3D11 \_ MAP \_ WRITE \_ DISCARD** al llamar a [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Escriba datos en la memoria.
3.  Llame [**a ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) cuando haya terminado de escribir datos.

## <a name="staging-usage"></a>Uso de almacenamiento provisional

Para rellenar una textura de almacenamiento provisional (una creada con **D3D11 \_ USAGE \_ STAGING**):

1.  Obtenga un puntero a la memoria de textura pasando **D3D11 \_ MAP \_ WRITE** al llamar a [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Escriba datos en la memoria.
3.  Llame [**a ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) cuando haya terminado de escribir datos.

Después, se puede usar una textura de almacenamiento provisional como parámetro de origen para [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) para rellenar un recurso predeterminado o dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




