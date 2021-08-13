---
description: En este documento se proporciona información sobre las consideraciones de seguridad relacionadas Windows adquisición de imágenes (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Consideraciones de seguridad: Windows de imágenes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb8f78e0f45b5b63d5d8deb8ffdd35bc64ee5566ced65ded30ecc51366c0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439702"
---
# <a name="security-considerations-windows-image-acquisition"></a>Consideraciones de seguridad: Windows de imágenes

En este documento se proporciona información sobre las consideraciones de seguridad relacionadas Windows adquisición de imágenes (WIA). Este documento no proporciona todo lo que necesita saber sobre los problemas de seguridad; en su lugar, úselo como punto de partida y referencia para esta área tecnológica.

-   [Usar comillas alrededor de los nombres de ruta de acceso](#use-quotation-marks-around-path-names)
-   [Colocación de aplicaciones registradas en ubicaciones seguras](#place-registered-applications-in-secure-locations)
-   [No use directorios subyacentes ni claves del Registro](#do-not-use-underlying-directories-or-registry-keys)
-   [Temas relacionados](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Usar comillas alrededor de los nombres de ruta de acceso

Al usar [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar una aplicación para recibir eventos de dispositivo, asegúrese de rodear la ruta de acceso y el nombre de archivo de la aplicación entre comillas. Esto evita la posibilidad de que la ruta de acceso se malinterprete y se ejecute una aplicación no autorizada.

## <a name="place-registered-applications-in-secure-locations"></a>Colocación de aplicaciones registradas en ubicaciones seguras

Cuando se registra una aplicación para recibir un evento de dispositivo, la puede ejecutar cualquier usuario que tenga acceso a ese dispositivo. Por ejemplo, si se registra una aplicación para un evento de examen, al presionar el botón "examinar" en un analizador, esa aplicación se ejecutará. Si la aplicación se ejecuta con un privilegio mayor que el que tiene el usuario, esto provoca un posible problema de seguridad.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>No use directorios subyacentes ni claves del Registro

WIA usa varios directorios y claves del Registro internamente para almacenar datos o información. No acceda directamente a estos directorios o claves del Registro. En su lugar, use los métodos de interfaz expuestos para especificar directorios para las imágenes adquiridas.

## <a name="related-topics"></a>Temas relacionados

-   [Seguridad de Microsoft](https://www.microsoft.com/security/)
-   [Página principal de seguridad de MSDN Library](https://msdn.microsoft.com/security/default.aspx)
-   [Recursos de acceso a la seguridad](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Recursos de seguridad de TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Consideraciones de seguridad para Windows desarrolladores de XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Procedimientos recomendados de seguridad](../secbp/best-practices-for-the-security-apis.md)

 

 
