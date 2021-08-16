---
description: Puede agregar compatibilidad con parámetros en tiempo de ejecución a un XAPO implementando la interfaz IXAPOParameters. La compatibilidad con parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf69fcc2570e26f188766a7f908a76d0dfcf3ec190d9fd0d7a1c434b242fdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805545"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a>Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO

Puede agregar compatibilidad con parámetros en tiempo de ejecución a un XAPO implementando la [**interfaz IXAPOParameters.**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) La compatibilidad con parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.

1.  Siga los pasos descritos [en Cómo: Crear un XAPO.](how-to--create-an-xapo.md)
2.  Cambie el XAPO para que se derive de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) y [**CXAPOBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
3.  Agregue llamadas a los [**métodos CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) y [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) a la implementación de [**IXAPO::P ).**](/windows/win32/api/xapo/nf-xapo-ixapo-process)

    > [!Note]  
    > La adición de estos métodos a [IXAPO::P procesos permite](how-to--build-a-basic-audio-processing-graph.md) a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantener sus copias de los parámetros de efecto en un estado seguro para subprocesos. Llame a [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) al principio de [**IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)y [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) al final de **IXAPO::P ).**

     

4.  Agregue más código a [**la implementación de IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para cambiar su comportamiento según los valores almacenados por el [**método SetParameters.**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)

    > [!Note]  
    > Agregar código al [**método IXAPO::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar los parámetros especificados por [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite cambiar el comportamiento de XAPO a lo largo de su vida.

     

5.  Al crear una instancia del efecto, asigne un búfer de tres de las estructuras que representarán los parámetros del efecto y pásales al constructor [**CXAPOParametersBase.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)

    > [!Note]  
    > La [**instancia de CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente este búfer para administrar los parámetros de efecto que se le pasan al llamar a [**SetParameters.**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) Debe inicializar todos los bloques de parámetros de proceso de *pParameterBlocks* en el mismo valor predeterminado antes de llamar a cualquiera de los métodos [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)e **IXAPOParameters::SetParameters.** Normalmente, esta inicialización se controla [**en IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) o [**en IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Información general de XAPO](xapo-overview.md)
</dt> </dl>

 

 
