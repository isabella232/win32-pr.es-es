---
title: Mensaje de DRV_LOAD (mmsystem. h)
description: Notifica al controlador que se ha cargado. El controlador debe asegurarse de que el hardware y los controladores auxiliares que necesita para funcionar correctamente estén presentes.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- Mensaje de DRV_LOAD de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997089"
---
# <a name="drv_load-message"></a>DRV \_ cargar mensaje

Notifica al controlador que se ha cargado. El controlador debe asegurarse de que el hardware y los controladores auxiliares que necesita para funcionar correctamente estén presentes.

## <a name="parameters"></a>Parámetros

El parámetro *hdrvr* siempre es cero. No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

El mensaje de **\_ carga DRV** es siempre el primer mensaje que recibe un controlador de dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> <dt>

[Mensajes de controlador instalables](installable-driver-messages.md)
</dt> </dl>

 

 





