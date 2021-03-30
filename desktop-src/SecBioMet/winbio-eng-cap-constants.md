---
title: Constantes de WINBIO_ENG_CAP (Winbio \_ Types. h)
description: Especifique las capacidades del motor genérico.
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d69db9f0e15ca0d50aa5ca134fdc74904dec85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803907"
---
# <a name="winbio_eng_cap-constants"></a>WINBIO \_ constantes de Cap de ENG \_

Las siguientes constantes son valores **de \_ funcionalidad de WINBIO** que se pueden usar para especificar las capacidades genéricas del componente del motor que está conectado a una unidad biométrica específica. Estas funcionalidades se especifican en el miembro **GenericEngineCapabilities** de la estructura de [**\_ \_ \_ información del motor extendido WINBIO**](winbio-extended-engine-info.md) .



| Constante o valor                                                                                                                                                                                                                                                                                        | Descripción                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Mejora iterativa de Cap de ENG**</dt> <dt>0x00000001</dt> </dl> | El componente del motor biométrico puede realizar una mejora iterativa.<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ \_Detección de \_ simulación \_ de Cap de ENG**</dt> <dt>0x00000002</dt> </dl>                   | El componente del motor biométrico puede realizar la detección de suplantaciones de identidad.<br/>       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



 

 





