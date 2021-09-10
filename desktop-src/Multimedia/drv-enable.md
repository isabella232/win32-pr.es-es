---
title: DRV_ENABLE mensaje (Mmsystem.h)
description: Habilita el controlador. El controlador debe inicializar cualquier variable y buscar dispositivos con la interfaz de entrada y salida (E/S).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370466"
---
# <a name="drv_enable-message"></a>Mensaje DE HABILITACIÓN DE DRV \_

Habilita el controlador. El controlador debe inicializar cualquier variable y buscar dispositivos con la interfaz de entrada y salida (E/S).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No se usan los parámetros *dwDriverId,* *lParam1* y *lParam2.*

Los controladores se consideran habilitados desde el momento en que reciben este mensaje hasta que se deshabilitan mediante el mensaje [**DISABLE \_ de DRV.**](drv-disable.md)

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

 

 





