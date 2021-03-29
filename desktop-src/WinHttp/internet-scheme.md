---
description: Esquemas de Internet compatibles con WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (winhttp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912410"
---
# <a name="internet_scheme"></a>esquema de INTERNET \_

Esquemas de Internet compatibles con WinHTTP.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**esquema de INTERNET \_ \_ http**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Un esquema HTTP de Internet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**esquema de INTERNET \_ \_ https**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Un esquema de Internet HTTPS (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**esquema de INTERNET \_ \_ FTP**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Un esquema de Internet FTP. Este esquema solo se admite para su uso en [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**esquema de INTERNET \_ \_ Socks**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un esquema de Internet SOCKS. Este esquema solo se admite para su uso en la [**\_ entrada de \_ resultados \_ del proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>   |
| Encabezado<br/>                   | <dl> <dt>Winhttp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_entrada de \_ resultado del proxy WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




