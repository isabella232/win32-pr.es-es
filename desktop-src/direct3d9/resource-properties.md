---
description: Todos los recursos comparten las siguientes propiedades.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Propiedades del recurso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9876b4d3befd48af917d6c11c71d5c8bbc7b0098f48b7c66ac28fb30bdbdb943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026125"
---
# <a name="resource-properties-direct3d-9"></a>Propiedades del recurso (Direct3D 9)

Todos los recursos comparten las siguientes propiedades.

-   Uso. La forma en que se usa un recurso, por ejemplo, como una textura o un destino de representación.
-   Formato. El formato de los datos, por ejemplo, el formato de píxel de una superficie 2D.
-   Piscina. Tipo de memoria donde se asigna el recurso.
-   Type (Tipo). El tipo de recurso, por ejemplo, un búfer de vértices o un destino de representación.

Se aplican los usos de recursos. Una aplicación que usará un recurso en una operación determinada debe especificar esa operación en el momento de la creación de recursos. Para obtener una lista de las constantes de uso definidas para los recursos, vea [**D3DUSAGE**](d3dusage.md).

Las constantes \_ D3DUSAGE RTPATCHES, D3DUSAGE NPATCHES y D3DUSAGE POINTS indican al controlador que es probable que los datos de estos búferes se usen para revisiones triangulares o de cuadrícula, N revisiones o sprites de \_ \_ punto, respectivamente. Estas marcas se proporcionan en caso de que el hardware no pueda realizar estas operaciones sin procesamiento de host. Por lo tanto, el controlador querrá asignar estas superficies en la memoria del sistema para que la CPU pueda acceder a ellas. Si el controlador puede realizar estas operaciones completamente en hardware, puede asignar estas superficies en vídeo o memoria AGP para evitar una copia del host y mejorar el rendimiento al menos por doble. Tenga en cuenta que la información proporcionada por estas marcas no es absolutamente necesaria. Un controlador puede detectar que estas operaciones se están realizando en los datos y volverá a mover el búfer a la memoria del sistema para los fotogramas posteriores.

Para más información sobre las marcas de uso y cómo se relacionan con recursos específicos, consulte las páginas de referencia de los métodos de creación de recursos individuales.

Para obtener información sobre el formato de superficie de los recursos, vea el tipo enumerado [D3DFORMAT.](d3dformat.md)

La clase de memoria que contiene los búferes de un recurso se denomina grupo. Los valores de grupo se definen mediante el tipo enumerado [**D3DPOOL.**](./d3dpool.md) Un grupo no se puede mezclar para distintos objetos contenidos en un único recurso (es decir, niveles mip en un mapa mip) y, cuando se elige un grupo para un recurso, el grupo no se puede cambiar.

Los tipos de recursos se establecen implícitamente en tiempo de ejecución cuando la aplicación llama a un método de creación de recursos como [**IDirect3DDevice9::CreateCubeTexture**](/windows/desktop/api). Los tipos de recursos se definen mediante el tipo enumerado [**D3DRESOURCETYPE.**](./d3dresourcetype.md) Las aplicaciones pueden consultar estos tipos en tiempo de ejecución; sin embargo, se espera que la mayoría de los escenarios no requieran la comprobación de tipos en tiempo de ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
