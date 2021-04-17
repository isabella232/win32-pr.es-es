---
title: Métodos (IInertiaProcessor)
description: Esta sección contiene los métodos de la interfaz IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interfaz IInertiaProcessor
- Windows Touch, métodos de interfaz
- inercia, interfaz IInertiaProcessor
- Interfaz IInertiaProcessor, métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714529"
---
# <a name="methods-iinertiaprocessor"></a>Métodos (IInertiaProcessor)

Esta sección contiene los métodos de la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Método                                                 | Descripción                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reset**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Inicializa el procesador con la marca de tiempo inicial y reinicia la inercia.                                                                                                                                                    |
| [**Proceso**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Realiza cálculos para la marca de tiempo actual y puede generar el evento **Delta** o **completed** dependiendo de si la extrapolación se ha completado o no. Si la extrapolación ha finalizado en el paso anterior, el método es no operativo. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Realiza cálculos para el paso dado y puede generar el evento **Delta** o **completed** dependiendo de si la extrapolación se ha completado o no.                                                                        |
| [**Completo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Finaliza la manipulación actual y detiene la inercia en el procesador de inercia.                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Finaliza la manipulación actual en el paso dado, detiene la inercia en el procesador de inercia y genera el evento ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




