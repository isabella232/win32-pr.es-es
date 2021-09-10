---
title: DRV_LOAD mensaje (Mmsystem.h)
description: Notifica al controlador que se ha cargado. El controlador debe asegurarse de que todos los controladores de hardware y de soporte que necesite para funcionar correctamente estén presentes.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370472"
---
# <a name="drv_load-message"></a>Mensaje DRV \_ LOAD

Notifica al controlador que se ha cargado. El controlador debe asegurarse de que todos los controladores de hardware y de soporte que necesite para funcionar correctamente estén presentes.

## <a name="parameters"></a>Parámetros

El *parámetro hdrvr* siempre es cero. No se usan los parámetros *dwDriverId,* *lParam1* y *lParam2.*

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero en caso contrario.

## <a name="remarks"></a>Observaciones

El **mensaje DRV \_ LOAD** siempre es el primer mensaje que recibe un controlador de dispositivo.

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

 

 





