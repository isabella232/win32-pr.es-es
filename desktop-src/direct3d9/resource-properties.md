---
description: Todos los recursos comparten las siguientes propiedades.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Propiedades de recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806524"
---
# <a name="resource-properties-direct3d-9"></a>Propiedades de recursos (Direct3D 9)

Todos los recursos comparten las siguientes propiedades.

-   Uso. La forma en que se utiliza un recurso, por ejemplo, como una textura o un destino de representación.
-   Formato. El formato de los datos, por ejemplo, el formato de píxel de una superficie 2D.
-   Fondo. El tipo de memoria en la que se asigna el recurso.
-   Type (Tipo). El tipo de recurso, por ejemplo, un búfer de vértice o un destino de representación.

Se aplican los usos de los recursos. Una aplicación que vaya a usar un recurso en una determinada operación debe especificar esa operación en el momento de la creación de recursos. Para obtener una lista de las constantes de uso definidas para los recursos, vea [**D3DUSAGE**](d3dusage.md).

Las \_ constantes D3DUSAGE RTPATCHES, D3DUSAGE \_ NPATCHES y D3DUSAGE \_ Points indican al controlador que los datos de estos búferes se usarán para las revisiones triangulares o cuadrículas, N-patch o sprites de punto, respectivamente. Estas marcas se proporcionan en caso de que el hardware no pueda realizar estas operaciones sin el procesamiento del host. Por lo tanto, el controlador querrá asignar estas superficies en la memoria del sistema para que la CPU pueda acceder a ellas. Si el controlador puede realizar estas operaciones completamente en hardware, puede asignar estas superficies en la memoria de vídeo o AGP para evitar una copia de host y mejorar el rendimiento al menos a la doble. Tenga en cuenta que la información proporcionada por estas marcas no es absolutamente necesaria. Un controlador puede detectar que dichas operaciones se realizan en los datos y que el búfer volverá a la memoria del sistema para los fotogramas posteriores.

Para obtener más información sobre las marcas de uso y cómo se relacionan con recursos específicos, vea las páginas de referencia en los métodos de creación de recursos individuales.

Para obtener información sobre el formato de superficie de los recursos, vea el tipo enumerado [D3DFORMAT](d3dformat.md) .

La clase de memoria que contiene los búferes de un recurso se denomina Grupo. Los valores de grupo se definen mediante el tipo enumerado [**D3DPOOL**](./d3dpool.md) . No se puede mezclar un grupo para los distintos objetos contenidos en un único recurso, es decir, los niveles de MIP en un mipmap y, cuando se elige un grupo para un recurso, el grupo no se puede cambiar.

Los tipos de recursos se establecen implícitamente en tiempo de ejecución cuando la aplicación llama a un método de creación de recursos como [**IDirect3DDevice9:: CreateCubeTexture**](/windows/desktop/api). Los tipos de recursos se definen mediante el tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) . Las aplicaciones pueden consultar estos tipos en tiempo de ejecución; sin embargo, se espera que la mayoría de los escenarios no requieran la comprobación de tipos en tiempo de ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
