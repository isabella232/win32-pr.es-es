---
description: Crypt32.dll es el módulo que implementa muchas de las funciones de CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809343"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll versiones

Crypt32.dll es el módulo que implementa muchas de las funciones de mensajería criptográfica y de certificado en la CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll es un módulo que se incluye con los sistemas operativos Windows y Windows Server, pero las distintas versiones de este archivo DLL proporcionan diferentes capacidades. No hay ninguna API para determinar la versión de CryptoAPI que está en uso, pero puede determinar la versión de Crypt32.dll que se está usando actualmente con las funciones [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) y [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

En general, los intervalos de versión de Crypt32.dll se asignan a las versiones del sistema operativo, tal como se muestra en la tabla siguiente. Sin embargo, esta tabla se debe utilizar como directriz solo porque es posible, a través de otras vías de actualización, que la versión Crypt32.dll diferirá de la indicada en la tabla.

| Versión de Crypt32.dll                               | Sistema operativo                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *versión* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *versión* >= 5.131.2600.1243                   | Windows XP con Service Pack 2 (SP2) Windows XP con Service Pack 1 (SP1) con la revisión [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *versión* < 5.131.2600.1243 | Windows XP con SP1Windows XP<br/>                                                                                                                                        |



 

 

 
