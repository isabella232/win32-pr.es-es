---
description: Para impulsar las actualizaciones visuales, la aplicación debe usar IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Motor de composición
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 14bc2ad60405dba7874493096e022b553a8b276cd6f0bb21ea9ae3cf191f5d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117905"
---
# <a name="composition-engine"></a>Motor de composición

Para impulsar las actualizaciones visuales, la aplicación debe usar [**IDirectManipulationCompositor.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) Este objeto es responsable de [](direct-manipulation-portal.md) actualizar los objetos visuales en función de las actualizaciones de manipulación directa, impulsar las actualizaciones de inercia y proporcionar información de control de tiempo de composición a la manipulación directa. Además, una aplicación debe usar el [DCompManipulationCompositor](direct-manipulation-guids.md) proporcionado por [manipulación](direct-manipulation-portal.md)directa, que controlará todas las actualizaciones visuales en nombre de la aplicación y controlará las actualizaciones de inercia.

[DCompManipulationCompositor](direct-manipulation-guids.md) es una implementación de la interfaz [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que encapsula [DirectComposition](../directcomp/directcomposition-portal.md). En lugar de que la aplicación aplique la salida, mediante este objeto [compositor, Manipulación](direct-manipulation-portal.md) directa puede aplicar la salida estableciendo las transformaciones directamente en el árbol DirectComposition. Con esta configuración, se puede procesar la entrada y se pueden aplicar transformaciones de salida, independientemente de la actividad en el subproceso de interfaz de usuario.

Para proporcionar [información de manipulación](direct-manipulation-portal.md) directa sobre el tiempo del motor de composición, la clase [DCompManipulationCompositor](direct-manipulation-guids.md) implementa la [**interfaz IDirectManipulationFrameInfoProvider.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) Al crear una ventanilla, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) es el puntero [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) obtenido de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para una instancia de **IDirectManipulationFrameInfoProvider**. El **puntero IDirectManipulationFrameInfoProvider** se pasa a la función [**IDirectManipulationManager::CreateViewport().**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)
