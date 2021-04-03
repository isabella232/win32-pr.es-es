---
title: Tipo de privacidad (Wininet. h)
description: Especifica que la configuración de privacidad es para cookies de terceros o de terceros.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905645"
---
# <a name="privacy-type"></a>Tipo de privacidad

Especifica que la configuración de privacidad es para cookies de terceros o de terceros.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo de privacidad de la \_ \_ primera \_ entidad**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Hace referencia a la configuración de privacidad de las cookies de primera entidad.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo de privacidad de \_ \_ terceros \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Hace referencia a la configuración de privacidad de las cookies de terceros.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Las cookies se clasifican como propias y de terceros. Una cookie de primera entidad es aquella que se origina desde el dominio del host. Si " https://www.blueyonderairlines.com " se encuentra en la barra de direcciones de Microsoft Internet Explorer, "www.blueyonderairlines.com" es el dominio del host. Al visitar esta página, si una cookie se establece desde un dominio que no sea "www.blueyonderairlines.com", como "www.fourthcoffee.com", se considera que esta cookie es una cookie de terceros.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

