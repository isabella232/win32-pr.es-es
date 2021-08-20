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
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966245"
---
# <a name="dynamic-reconnection-flags"></a>Marcas de reconexión dinámica

\[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

Las marcas siguientes especifican el nivel de reconexión dinámica que se usará durante la representación.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | No hay reconexión dinámica. Cargue todo antes de representar el proyecto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ Orígenes \_ dinámicos**</dt> <dt>0x01</dt> </dl> | Cargue los orígenes solo según sea necesario.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ Efectos \_ dinámicos**</dt> <dt>0x02</dt> </dl> | Reservado. No utilizar.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




