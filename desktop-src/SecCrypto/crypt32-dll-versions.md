---
description: Crypt32.dll es el módulo que implementa muchas de las funciones cryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fed9fb7e31af86673c4d24a9dd828c8d690441986725026f982c0720753c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876475"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll versiones anteriores

Crypt32.dll es el módulo que implementa muchas de las funciones De certificado y Mensajería criptográfica en CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll es un módulo que se incluye con los sistemas operativos Windows y Windows Server, pero las distintas versiones de este archivo DLL proporcionan diferentes funcionalidades. No hay ninguna API para determinar la versión de CryptoAPI que está en uso, pero puede determinar la versión de Crypt32.dll que está actualmente en uso mediante las funciones [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) y [**VerQueryValue.**](/windows/win32/api/winver/nf-winver-verqueryvaluea)

En general, los intervalos de versiones de Crypt32.dll se asignan a las versiones del sistema operativo, como se muestra en la tabla siguiente. Sin embargo, esta tabla solo debe usarse como guía porque es posible, a través de otras vías de actualización, que la versión de Crypt32.dll sea diferente de la indicada en la tabla.

| Crypt32.dll versión                               | Sistema operativo                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *version* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *version* >= 5.131.2600.1243                   | Windows XP con Service Pack 2 (SP2)Windows XP con Service Pack 1 (SP1) con [revisión Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *versión* < 5.131.2600.1243 | Windows XP con SP1Windows XP<br/>                                                                                                                                        |



 

 

 
