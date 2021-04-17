---
description: Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico del descodificador de nivel superior.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680233"
---
# <a name="ec_vmr_reconnection_failed"></a>\_error de \_ reconexión de VMR de EC \_

Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico del descodificador de nivel superior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de estado devuelto por [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada de VMR que no pudo reconectar.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento se reenvía a las aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




