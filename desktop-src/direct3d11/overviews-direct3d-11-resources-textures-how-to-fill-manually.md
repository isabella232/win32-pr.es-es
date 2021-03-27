---
title: Cómo inicializar una textura mediante programación
description: En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas que se crean con distintos tipos de usos.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903614"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Cómo: inicializar una textura mediante programación

Puede inicializar una textura durante la creación del objeto o puede rellenar el objeto mediante programación una vez creado. En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas que se crean con distintos tipos de usos. En este ejemplo se da por supuesto que ya sabe cómo [crear una textura](overviews-direct3d-11-resources-textures-create.md).

-   [Uso predeterminado](#default-usage)
-   [Uso dinámico](#dynamic-usage)
-   [Uso del almacenamiento provisional](#staging-usage)
-   [Temas relacionados](#related-topics)

## <a name="default-usage"></a>Uso predeterminado

El tipo de uso más común es el uso predeterminado. Para rellenar una textura predeterminada (una creada con el **\_ \_ valor predeterminado de uso de D3D11**), puede:

-   Llame a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inicialice *pInitialData* para apuntar a los datos proporcionados por una aplicación.

    o

-   Después de llamar a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para rellenar la textura predeterminada con los datos de un puntero proporcionado por la aplicación.

## <a name="dynamic-usage"></a>Uso dinámico

Para rellenar una textura dinámica (una creada con el **uso de D3D11 \_ \_ dinámica**):

1.  Obtener un puntero a la memoria de textura pasando el **\_ \_ \_ descartado de escritura de asignación de D3D11** al llamar a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Escribir datos en la memoria.
3.  Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar cuando termine de escribir los datos.

## <a name="staging-usage"></a>Uso del almacenamiento provisional

Para rellenar una textura de ensayo (una creada con el **\_ \_ almacenamiento provisional del uso de D3D11**):

1.  Obtenga un puntero a la memoria de textura pasando en la **D3D11 de \_ \_ escritura de asignación** al llamar a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Escribir datos en la memoria.
3.  Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar cuando termine de escribir los datos.

Después, se puede usar una textura de ensayo como parámetro de origen para [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) para rellenar un recurso predeterminado o dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Texturas](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




