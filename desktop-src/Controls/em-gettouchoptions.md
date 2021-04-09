---
title: Mensaje EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera las opciones de toque que están asociadas a un control Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079611"
---
# <a name="em_gettouchoptions-message"></a>\_Mensaje GETTOUCHOPTIONS em

Recupera las opciones de toque que están asociadas a un control Rich Edit.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Opciones de toque que se van a recuperar. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                        | Significado                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Recupera si las redimensionamientos táctiles están visibles.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | No se ha implementado la recuperación de esta marca.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la opción especificada por el parámetro *wParam* . Es distinto de cero si *wParam* es **RTO \_ SHOWHANDLES** y las redimensionadores táctiles son visibles; de lo contrario, es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 





