---
title: Mensaje de PSM_UNCHANGED (Prsht. h)
description: Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ sin cambios.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274546"
---
# <a name="psm_unchanged-message"></a>Mensaje de PSM \_ sin cambios

Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la macro [**PropSheet \_ sin cambios**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la página que se ha revertido al estado guardado anteriormente.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La hoja de propiedades deshabilita el botón **aplicar** si ninguna otra página tiene cambios registrados con la hoja de propiedades.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





