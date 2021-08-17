---
title: Tipo de privacidad (Wininet.h)
description: Especifica que la configuración de privacidad es para cookies propias o de terceros.
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
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743732"
---
# <a name="privacy-type"></a>Tipo de privacidad

Especifica que la configuración de privacidad es para cookies propias o de terceros.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY \_ TYPE \_ FIRST \_ PARTY**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Hace referencia a la configuración de privacidad de las cookies propias.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**TIPO \_ DE PRIVACIDAD DE \_ \_ TERCEROS**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Hace referencia a la configuración de privacidad de las cookies de terceros.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Las cookies se clasifican como propias y de terceros. Una cookie de origen es aquella que se origina en el dominio host. Si " " se encuentra en la barra de Internet Explorer de https://www.blueyonderairlines.com Microsoft, "www.blueyonderairlines.com" es el dominio host. Al visitar esta página, si una cookie se establece desde un dominio distinto de "www.blueyonderairlines.com", como "www.fourthcoffee.com", esta cookie se considera una cookie de terceros.

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

