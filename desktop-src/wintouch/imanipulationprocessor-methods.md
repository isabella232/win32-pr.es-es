---
title: Métodos (IInertiaProcessor)
description: Esta sección contiene los métodos para la interfaz IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Interfaz Touch,IInertiaProcessor
- Windows Métodos touch,interface
- inertia,IInertiaProcessor (interfaz)
- IInertiaProcessor interface,methods
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cb5c03039c09ef1435fcddd4782a466fff3aa179d57e5abb3887fa9212ca753
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881445"
---
# <a name="methods-iinertiaprocessor"></a>Métodos (IInertiaProcessor)

Esta sección contiene los métodos para la [**interfaz IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)



| Método                                                 | Descripción                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Restablecer**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Inicializa el procesador con la marca de tiempo inicial y reinicia la inercia.                                                                                                                                                    |
| [**Proceso**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Realiza cálculos para el tic actual y puede generar el evento **Delta** o **Completed** en función de si la extrapolación se ha completado o no. Si la extrapolación finalizó en el tic anterior, el método no es operativo. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Realiza cálculos para el tic dado y puede generar el evento **Delta** o **Completed** en función de si la extrapolación se ha completado o no.                                                                        |
| [**Completo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Finaliza la manipulación actual y detiene la inercia en el procesador de inercia.                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Finaliza la manipulación actual en el tic especificado, detiene la inercia en el procesador de inercia y genera el evento ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




