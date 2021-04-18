---
description: Para impulsar las actualizaciones visuales, la aplicación debe usar IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Motor de composición
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494951"
---
# <a name="composition-engine"></a>Motor de composición

Para impulsar las actualizaciones visuales, la aplicación debe usar [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Este objeto es responsable de actualizar los objetos visuales en función de las actualizaciones de la [manipulación directa](direct-manipulation-portal.md) , impulsar las actualizaciones de inercia hacia delante y proporcionar información sobre el tiempo de composición para la manipulación directa. Además, una aplicación debe usar el [DCompManipulationCompositor](direct-manipulation-guids.md) proporcionado por la [manipulación directa](direct-manipulation-portal.md), que controlará todas las actualizaciones visuales en nombre de la aplicación y las actualizaciones de inercia.

[DCompManipulationCompositor](direct-manipulation-guids.md) es una implementación de la interfaz [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que contiene [DirectComposition](../directcomp/directcomposition-portal.md). En lugar de que la aplicación aplique la salida, a través de este objeto de compositor, la [manipulación directa](direct-manipulation-portal.md) puede aplicar la salida mediante el establecimiento de las transformaciones directamente en el árbol DirectComposition. Con esta configuración, se puede procesar la entrada y se pueden aplicar transformaciones de salida, independientemente de la actividad en el subproceso de la interfaz de usuario.

Para proporcionar información de [manipulación directa](direct-manipulation-portal.md) en el momento del motor de composición, la clase [DCompManipulationCompositor](direct-manipulation-guids.md) implementa la interfaz [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) . Al crear una ventanilla, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) el puntero [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) Obtenido de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para una instancia de **IDirectManipulationFrameInfoProvider**. El puntero **IDirectManipulationFrameInfoProvider** se pasa a la función [**IDirectManipulationManager:: CreateViewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) .
