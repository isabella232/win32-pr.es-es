---
title: Interfaces de DirectML
description: Las interfaces siguientes se declaran en DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 64ae11c5b9a4298c340488499a5a309b71a2d48b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249099"
---
# <a name="directml-interfaces"></a>Interfaces de DirectML

Las interfaces siguientes se declaran en DirectML.h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra los envíos de trabajo de DirectML en una lista de comandos de Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Representa una forma compilada y eficaz de un operador adecuado para su ejecución en la GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controla la capa de depuración de DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Representa un dispositivo DirectML, que se usa para crear operadores, tablas de enlace, grabadoras de comandos y otros objetos. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Representa un dispositivo DirectML, que se usa para crear operadores, tablas de enlace, grabadoras de comandos y otros objetos. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Interfaz implementada por todos los objetos creados a partir del dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementado por objetos que se pueden grabar en una lista de comandos para su distribución en la GPU, mediante [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmlobject) | Interfaz de la que [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) e [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) heredan directamente (y todas las demás interfaces, indirectamente). Por lo tanto, proporciona métodos comunes a todas las interfaces de DirectML, específicamente los métodos para asociar datos privados y anotar nombres de objeto. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Representa un operador DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Representa un objeto especializado cuyo propósito es inicializar operadores compilados. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implementado por objetos que se pueden expulsar de la memoria de GPU y, por lo tanto, se puede proporcionar a [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice::MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
