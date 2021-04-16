---
description: Las marcas siguientes especifican el nivel de reconexión dinámica que se va a usar durante la representación.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Marcas de reconexión dinámica (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679429"
---
# <a name="dynamic-reconnection-flags"></a>Marcas de reconexión dinámica

\[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

Las marcas siguientes especifican el nivel de reconexión dinámica que se va a usar durante la representación.



| Constante o valor                                                                                                                                                                                                                                            | Descripción                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_ DYNAMIC \_ None**</dt> <dt>0x00</dt> </dl>          | Sin reconexión dinámica. Cargue todo antes de representar el proyecto.<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_ \_Orígenes dinámicos**</dt> <dt>0x01</dt> </dl> | Cargar solo los orígenes según sea necesario.<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_ \_Efectos dinámicos**</dt> <dt>0x02</dt> </dl> | Reservado. No utilizar.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




