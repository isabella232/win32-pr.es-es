---
description: Puede Agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO implementando la interfaz IXAPOParameters. La compatibilidad de parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497638"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO

Puede Agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO implementando la interfaz [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . La compatibilidad de parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.

1.  Siga los pasos [que se describen en cómo: crear un XAPO](how-to--create-an-xapo.md).
2.  Cambie XAPO para que derive de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) y [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).
3.  Agregue llamadas a los métodos [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) y [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) a la implementación de [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

    > [!Note]  
    > Agregar estos métodos a [IXAPO::P rador](how-to--build-a-basic-audio-processing-graph.md) permite a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantener sus copias de los parámetros de efecto en un estado seguro para subprocesos. Llame a [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) al principio de [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process)y [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) al final de **IXAPO::P rador**.

     

4.  Agregue más código a la implementación [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para cambiar su comportamiento en función de los valores almacenados por el método [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .

    > [!Note]  
    > Agregar código al método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar los parámetros especificados por [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite cambiar el comportamiento del XAPO a lo largo de su vida.

     

5.  Cuando se crea una instancia del efecto, se asigna un búfer de tres de las estructuras que representan los parámetros del efecto y se pasa al constructor [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

    > [!Note]  
    > La instancia de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente este búfer para administrar los parámetros de efecto que se le pasan cuando se llama a [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters). Debe inicializar todos los bloques de parámetros de proceso de *pParameterBlocks* en el mismo valor predeterminado antes de llamar a cualquiera de los métodos [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)y **IXAPOParameters:: SetParameters** . Normalmente, esta inicialización se controla en [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) o en [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Información general de XAPO](xapo-overview.md)
</dt> </dl>

 

 
