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
ms.openlocfilehash: 83fc0097896af0ad18ff89895eb8c5debc36e196e1687fc9706c655b4ec95d48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088465"
---
# <a name="psm_unchanged-message"></a>Mensaje PSM \_ UNCHANGED

Informa a una hoja de propiedades de que la información de una página ha revertido al estado guardado anteriormente. Puede enviar este mensaje explícitamente o mediante la [**macro PropSheet \_ UnChanged.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la página que ha revertido al estado guardado anteriormente.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La hoja de propiedades deshabilita el botón **Aplicar** si ninguna otra página ha registrado cambios en la hoja de propiedades.

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





