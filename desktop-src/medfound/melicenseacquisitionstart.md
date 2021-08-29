---
description: Lo genera el motor de directivas cuando la adquisición de licencias está a punto de comenzar. La adquisición de licencias se realiza mediante la implementación de aplicaciones de la interfaz IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Evento MELicenseAcquisitionStart (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea326ff23c4d546f0b692a813ef92ccfce8e3cc97320a8129daa9cedc4867bfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228975"
---
# <a name="melicenseacquisitionstart-event"></a>Evento MELicenseAcquisitionStart

Lo genera el motor de directivas cuando la adquisición de licencias está a punto de comenzar. La adquisición de licencias se realiza mediante la implementación de la aplicación de la [**interfaz IMFContentProtectionManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Cuando se completa la adquisición de licencias, el motor de directivas genera el [evento MELicenseAcquisitionCompleted.](melicenseacquisitioncompleted.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




