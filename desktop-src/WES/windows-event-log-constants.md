---
title: Constantes del registro de eventos de Windows (WinEvt. h)
description: 'El registro de eventos de Windows define las constantes siguientes:'
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422290"
---
# <a name="windows-event-log-constants"></a>Constantes del registro de eventos de Windows

El registro de eventos de Windows define las constantes siguientes:

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT \_ variante \_ Type \_ Mask**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Máscara de bits que se usa para enmascarar el bit de la matriz del tipo variante, de modo que pueda determinar el tipo de datos del valor Variant que contiene la estructura de la [**\_ variante evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT \_ variante \_ Type \_ array**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



El miembro de **tipo** de la estructura [**evt \_ Variant**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) tiene este bit establecido si la variante contiene un puntero a una matriz de valores, en lugar del propio valor.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT \_ - \_ acceso de lectura**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Permiso de control de acceso de lectura que permite leer información de un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_acceso de escritura de EVT \_**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Permiso de control de acceso de escritura que permite escribir información en un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT \_ - \_ acceso sin formato**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Permiso Clear Access Control que permite borrar toda la información de un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ All \_ Access**
</dt> <dd> <dl> <dt>

0X7
</dt> <dt>



Todos los permisos de control de acceso (lectura, escritura, borrado y eliminación).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





