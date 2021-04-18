---
description: Los siguientes GUID de clase de manipulación directa se definen en DirectManipulation. idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUID de manipulación directa
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105720260"
---
# <a name="direct-manipulation-guids"></a>GUID de manipulación directa

Los siguientes GUID de clase de [manipulación directa](direct-manipulation-portal.md) se definen en DirectManipulation. idl.

- [Clase maestra: identificadores](#master-class-ids)
- [Clase de contenido secundario: identificadores](#secondary-content-class-ids)
- [Clase de objetos Behavior: identificadores](#behavior-objects-class-ids)
- [Temas relacionados](#related-topics)

## <a name="master-class-ids"></a>Clase maestra: identificadores

| GUID                                     | Descripción                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | Clase DirectManipulationManager. Este objeto proporciona acceso a todas las características de [manipulación directa](direct-manipulation-portal.md) y a las API disponibles para la aplicación.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | Clase DCompManipulationCompositor. Se trata de una implementación de [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que incluye DirectComposition. A través de este objeto compositor DirectManipulation puede aplicar el resultado estableciendo transformaciones directamente en el árbol DComp. |

## <a name="secondary-content-class-ids"></a>Clase de contenido secundario: identificadores

| GUID                                  | Descripción                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indicador de movimiento panorámico vertical. Elemento visual que muestra la posición actual en el contenido que se extiende fuera de la pantalla verticalmente.     |
| **CLSID \_ HorizontalIndicatorContent** | Indicador de movimiento panorámico horizontal. Elemento visual que muestra la posición actual en el contenido que se extiende horizontalmente fuera de la pantalla. |
| **CLSID \_ VirtualViewportContent**     | Ventanilla virtual. Una ventanilla virtual se puede usar para respetar los elementos de posición fijos para las ventanillas con zoom configurado.          |

## <a name="behavior-objects-class-ids"></a>Clase de objetos Behavior: identificadores

| GUID                                     | Descripción                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Arrastre & comportamiento de colocación. Permite seleccionar y arrastrar los elementos.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Comportamiento de desplazamiento automático. Permite que el contenido se desplace automáticamente a medida que se aproxima al límite de un eje determinado.                                           |
| **CLSID \_ DeferContactService**           | Comportamiento de aplazamiento de contacto. Cantidad de tiempo (en millliseconds) que se va a esperar antes de llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Temas relacionados

[Manipulación directa](direct-manipulation-portal.md), [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration), [**AddConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration), [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
