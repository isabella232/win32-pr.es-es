---
title: Funciones de moniker de dirección URL
description: Funciones de moniker de dirección URL
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db726d8ce6a101b0b97fbe2128e074ee5e892e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160520"
---
# <a name="url-moniker-functions"></a>Funciones de moniker de dirección URL

Las funciones de moniker de url aíslan a los desarrolladores de las complejidades de crear, administrar y usar monikers de direcciones URL. Estas funciones son las siguientes:

-   [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

Su familiaridad con estas funciones puede ser la siguiente:

-   Familiarícese [**con CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) [**e IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) si va a usar monikers de dirección URL en aplicaciones independientes. Si va a crear un control ActiveX, debe usar [**IBindHost::CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) en lugar de **CreateURLMoniker**.
-   Familiarícese [**con RegisterMediaTypes,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) [**CreateFormatEnumerator,**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator) [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))y [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) si va a realizar cualquier negociación MIME con monikers de url.
-   Familiarícese con [**RegisterMediaTypeClass,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)) [**FindMediaTypeClass,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)) [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))y [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) solo si tiene una experiencia significativa con los monikers de url y con COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 