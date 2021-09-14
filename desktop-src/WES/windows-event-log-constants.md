---
title: Windows Constantes del registro de eventos (WinEvt.h)
description: Windows El registro de eventos define las constantes siguientes
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241527"
---
# <a name="windows-event-log-constants"></a>Windows Constantes del registro de eventos

Windows El registro de eventos define las constantes siguientes:

<dl> <dt>

<span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT \_ VARIANT \_ TYPE \_ MASK**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



Máscara de bits que se usa para enmascarar el bit de matriz del tipo de variante, por lo que puede determinar el tipo de datos del valor de variante que contiene la estructura [**\_ VARIANT de EVT.**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant)


</dt> </dl> </dd> <dt>

<span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT \_ VARIANT \_ TYPE \_ ARRAY**
</dt> <dd> <dl> <dt>

128
</dt> <dt>



El **miembro Type** de la estructura [**EVT \_ VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) tiene este bit establecido si la variante contiene un puntero a una matriz de valores, en lugar del propio valor.


</dt> </dl> </dd> <dt>

<span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**ACCESO DE \_ LECTURA EVT \_**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Permiso de control de acceso de lectura que permite leer información de un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**ACCESO DE \_ ESCRITURA EVT \_**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Permiso de control de acceso de escritura que permite escribir información en un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT \_ CLEAR \_ ACCESS**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Desactive el permiso de control de acceso que permite borrar toda la información de un registro de eventos.


</dt> </dl> </dd> <dt>

<span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Todos los permisos de control de acceso (lectura, escritura, borrado y eliminación).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>WinEvt.h</dt> </dl> |



 

 





