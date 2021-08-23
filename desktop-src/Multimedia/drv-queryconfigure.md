---
title: DRV_QUERYCONFIGURE mensaje (Mmsystem.h)
description: Indica al controlador que especifique si admite la configuración personalizada.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c49ec54d1822bbc9ddc4d2606f8905a21c5193322a12df335549074dacdea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691575"
---
# <a name="drv_queryconfigure-message"></a>DRV \_ QUERYCONFIGURE message

Indica al controlador que especifique si admite la configuración personalizada.

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

Devuelve un valor distinto de cero si el controlador puede mostrar un cuadro de diálogo de configuración o cero en caso contrario.

## <a name="remarks"></a>Comentarios

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

 

 





