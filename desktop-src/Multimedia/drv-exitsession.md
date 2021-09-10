---
title: DRV_EXITSESSION mensaje (Mmsystem.h)
description: Notifica al controlador que Windows está preparando la salida. El controlador debe prepararse para la terminación.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- DRV_EXITSESSION mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370484"
---
# <a name="drv_exitsession-message"></a>Mensaje \_ EXITSESSION de DRV

Notifica al controlador que Windows está preparando la salida. El controlador debe prepararse para la terminación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador del controlador instalable. Este es el mismo valor devuelto anteriormente por el controlador del [**mensaje DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No se usan los parámetros *lParam1* y *lParam2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> <dt>

[Mensajes de controlador instalables](installable-driver-messages.md)
</dt> </dl>

 

 





