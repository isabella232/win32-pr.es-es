---
description: Los siguientes GUID de direct manipulation class se definen en DirectManipulation.idl.
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: GUID de manipulación directa
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3ee67206bf9395c3a338dba27c9365578d30d7304f465d93fdc90322a77a8a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280546"
---
# <a name="direct-manipulation-guids"></a>GUID de manipulación directa

Los siguientes [GUID de direct manipulation](direct-manipulation-portal.md) class se definen en DirectManipulation.idl.

- [Master class-IDs (IDs de clase maestra)](#master-class-ids)
- [IDs de clase de contenido secundario](#secondary-content-class-ids)
- [Objetos de comportamiento:IDs de clase](#behavior-objects-class-ids)
- [Temas relacionados](#related-topics)

## <a name="master-class-ids"></a>Master class-IDs (IDs de clase maestra)

| GUID                                     | Descripción                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | DirectManipulationManager (clase). Este objeto proporciona acceso a todas las [API](direct-manipulation-portal.md) y características de manipulación directa disponibles para la aplicación.                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | DCompManipulationCompositor (clase). Se trata de una implementación de [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) que encapsula DirectComposition. A través de este objeto compositor, DirectManipulation puede aplicar la salida estableciendo transformaciones directamente en el árbol DComp. |

## <a name="secondary-content-class-ids"></a>IDs de clase de contenido secundario

| GUID                                  | Descripción                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | Indicador de movimiento panorámico vertical. Elemento visual que muestra la posición actual en el contenido que se extiende verticalmente fuera de la pantalla.     |
| **CLSID \_ HorizontalIndicatorContent** | Indicador de desplazamiento horizontal. Elemento visual que muestra la posición actual en el contenido que se extiende horizontalmente fuera de la pantalla. |
| **CLSID \_ VirtualViewportContent**     | Ventanilla virtual. Se puede usar una ventanilla virtual para respetar los elementos de posición fija de las ventanillas con zoom configurado.          |

## <a name="behavior-objects-class-ids"></a>Objetos de comportamiento:IDs de clase

| GUID                                     | Descripción                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | Arrastre & Comportamiento de colocación. Permite seleccionar y arrastrar elementos.                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Comportamiento de la inscripción automática. Permite que el contenido se desplace automáticamente a medida que se aproxima al límite de un eje determinado.                                           |
| **CLSID \_ DeferContactService**           | Comportamiento de aplazamiento de contacto. Cantidad de tiempo (en millones de segundos) que se debe esperar antes de llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). |

## <a name="related-topics"></a>Temas relacionados

[Manipulación directa,](direct-manipulation-portal.md) [**ActivateConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration) [**AddConfiguration,**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration) [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
