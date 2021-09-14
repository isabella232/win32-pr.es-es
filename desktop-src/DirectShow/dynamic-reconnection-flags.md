---
description: Las marcas siguientes especifican el nivel de reconexión dinámica que se usará durante la representación.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Marcas de reconexión dinámica (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061215"
---
# <a name="dynamic-reconnection-flags"></a>Marcas de reconexión dinámica

\[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

Las marcas siguientes especifican el nivel de reconexión dinámica que se usará durante la representación.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | Sin reconexión dinámica. Cargue todo antes de representar el proyecto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ Orígenes \_ dinámicos**</dt> <dt>0x01</dt> </dl> | Cargue los orígenes solo según sea necesario.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ Efectos \_ dinámicos**</dt> <dt>0x02</dt> </dl> | Reservado. No utilizar.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




