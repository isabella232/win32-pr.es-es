---
title: EM_SETTOUCHOPTIONS mensaje (Richedit.h)
description: Establece las opciones táctiles asociadas a un control de edición enriquecido.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048019"
---
# <a name="em_settouchoptions-message"></a>Mensaje \_ EM SETTOUCHOPTIONS

Establece las opciones táctiles asociadas a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Opción táctil que se establece. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Muestre u oculte los identificadores de control táctil, en función del valor *de lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Habilite o deshabilite los controladores de control táctil, en función del valor *de lParam*. Cuando los identificadores están deshabilitados, se ocultan si están visibles y permanecen ocultos hasta que un **mensaje \_ SETTOUCHOPTIONS de EM** cambia su estado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Establezca en **TRUE para** mostrar o habilitar los identificadores de selección táctil, o **FALSE** para ocultar o deshabilitar los identificadores de selección táctil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





