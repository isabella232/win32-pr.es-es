---
title: DRV_LOAD mensaje (Mmsystem.h)
description: Notifica al controlador que se ha cargado. El controlador debe asegurarse de que todos los controladores de hardware y de soporte que necesita para funcionar correctamente estén presentes.
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
ms.openlocfilehash: d74b8d0663e96f0dc700739c7b8b5f9304d478ed02bf9493f24d03a506c14a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678715"
---
# <a name="drv_load-message"></a>Mensaje DE CARGA DE DRV \_

Notifica al controlador que se ha cargado. El controlador debe asegurarse de que todos los controladores de hardware y de soporte que necesita para funcionar correctamente estén presentes.

## <a name="parameters"></a>Parámetros

El *parámetro hdrvr* siempre es cero. No se usan los parámetros *dwDriverId,* *lParam1* y *lParam2.*

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero de lo contrario.

## <a name="remarks"></a>Comentarios

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

 

 





