---
title: EM_GETTOUCHOPTIONS mensaje (Richedit.h)
description: Recupera las opciones táctiles asociadas a un control de edición enriquecido.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS controles de Windows mensaje
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
ms.openlocfilehash: f4771cd11fd8aaf16925c97a3242918ba8f7b56e4e580a6f3cd70672a134399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799995"
---
# <a name="em_gettouchoptions-message"></a>Mensaje \_ DE EM GETTOUCHOPTIONS

Recupera las opciones táctiles asociadas a un control de edición enriquecido.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Opciones táctiles que se recuperarán. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                        | Significado                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Recupera si los controladores táctiles están visibles.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | No se implementa la recuperación de esta marca.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la opción especificada por el *parámetro wParam.* Es distinto de cero si *wParam* es **RTO \_ SHOWHANDLES** y los controladores táctiles están visibles; cero, en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





