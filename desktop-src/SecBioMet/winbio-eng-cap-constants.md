---
title: WINBIO_ENG_CAP constantes (Winbio \_ types.h)
description: Especifique las funcionalidades genéricas del motor.
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
ms.openlocfilehash: a5be1099b6ad555b0547dc975c1446740f43359792c1643d155322095ad26dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867955"
---
# <a name="winbio_eng_cap-constants"></a>Constantes CAP de WINBIO \_ ENG \_

Las siguientes constantes son valores **DE \_ FUNCIONALIDADES** DE WINBIO que se pueden usar para especificar funcionalidades genéricas del componente del motor que está conectado a una unidad biométrica específica. Estas funcionalidades se especifican en **el miembro GenericEngineCapabilities** de la [**estructura WINBIO EXTENDED ENGINE \_ \_ \_ INFO.**](winbio-extended-engine-info.md)



| Constante o valor                                                                                                                                                                                                                                                                                        | Descripción                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ MEJORAS \_ \_ ITERATIVAS \_ ENG CAP**</dt> <dt>0X00000001</dt> </dl> | El componente del motor biométrico puede realizar una mejora iterativa.<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ DETECCIÓN \_ DE \_ SUPLANTACIÓN DE LÍMITE \_ DE ENG**</dt> <dt>0x00000002</dt> </dl>                   | El componente del motor biométrico puede realizar la detección de suplantación.<br/>       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



 

 





