---
title: Interfaces de DirectML
description: Las siguientes interfaces se declaran en DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 9752b52f1d9a311a1ada6b609a86691a336b77e7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "105665891"
---
# <a name="directml-interfaces"></a>Interfaces de DirectML

Las siguientes interfaces se declaran en DirectML. h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crea un dispositivo DirectML para un dispositivo Direct3D 12 determinado. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra los envíos del trabajo de DirectML en una lista de comandos de Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Representa una forma compilada y eficaz de un operador adecuado para su ejecución en la GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controla la capa de depuración DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Representa un dispositivo DirectML, que se usa para crear operadores, enlazar tablas, grabadores de comandos y otros objetos. |
| [**IDMLDevice1**](/windows/desktop/direct3d12/directml/nn-directml-idmldevice1) | Representa un dispositivo DirectML, que se usa para crear operadores, enlazar tablas, grabadores de comandos y otros objetos. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Una interfaz implementada por todos los objetos creados desde el dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementado por objetos que se pueden grabar en una lista de comandos para su distribución en la GPU, mediante [IDMLCommandRecorder:: RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmlobject) | Una interfaz de la que [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) y [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) heredan directamente (y todas las demás interfaces, indirectamente). Por consiguiente, proporciona métodos comunes a todas las interfaces DirectML, específicamente métodos para asociar datos privados y anotar nombres de objeto. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Representa un operador DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Representa un objeto especializado cuyo propósito es inicializar los operadores compilados. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Lo implementan los objetos que se pueden desalojar de la memoria de GPU y, por lo tanto, se pueden proporcionar a [IDMLDevice:: expulsión](/windows/desktop/api/directml/nf-directml-idmldevice-evict) y [IDMLDevice:: MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de DirectML](direct3d-directml-reference.md)
* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
