---
title: Mensaje EM_SETTOUCHOPTIONS (RichEdit. h)
description: Establece las opciones de toque asociadas a un control Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS controles de mensajes de Windows
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
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491200"
---
# <a name="em_settouchoptions-message"></a>\_Mensaje SETTOUCHOPTIONS em

Establece las opciones de toque asociadas a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Opción de toque que se va a establecer. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Mostrar u ocultar los controladores de la agarrador táctil, dependiendo del valor de *lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Habilitar o deshabilitar los identificadores de la agarración táctil, dependiendo del valor de *lParam*. Cuando se deshabilitan los identificadores, se ocultan si están visibles y permanecen ocultos hasta que un mensaje **\_ SETTOUCHOPTIONS em** cambia su estado. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Establézcalo en **true** para mostrar/habilitar los manipuladores de la selección táctil, o en **false** para ocultar o deshabilitar los controladores de selección táctil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





