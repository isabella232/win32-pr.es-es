---
description: Esquemas de Internet compatibles con WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0429d07ef366acdc881a82373194e153ad3c8f367172b7e64221ecf479e7bf3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644025"
---
# <a name="internet_scheme"></a>ESQUEMA \_ DE INTERNET

Esquemas de Internet compatibles con WinHTTP.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**HTTP \_ DE ESQUEMA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Un esquema http de Internet.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**HTTPS \_ DE ESQUEMA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Esquema de Internet HTTPS (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP DE ESQUEMA DE \_ INTERNET**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Un esquema ftp de Internet. Este esquema solo se admite para su uso [**en WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) y [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**MEDIAS \_ DE ESQUEMA DE INTERNET \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un esquema de Internet SOCKS. Este esquema solo se admite para su uso en [**WINHTTP \_ PROXY RESULT \_ \_ ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>      |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>   |
| Header<br/>                   | <dl> <dt>Winhttp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ENTRADA DE \_ RESULTADOS DEL PROXY \_ \_ WINHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




