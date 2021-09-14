---
title: PSM_UNCHANGED mensaje (Prsht.h)
description: Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la macro PropSheet \_ UnChanged.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167461"
---
# <a name="psm_unchanged-message"></a>Mensaje PSM \_ UNCHANGED

Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ UnChanged.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la página que ha revertido al estado guardado previamente.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La hoja de propiedades deshabilita el **botón Aplicar** si ninguna otra página ha registrado cambios con la hoja de propiedades.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





