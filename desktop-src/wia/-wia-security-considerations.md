---
description: En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la adquisición de imágenes de Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Consideraciones de seguridad: adquisición de imágenes de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715183"
---
# <a name="security-considerations-windows-image-acquisition"></a>Consideraciones de seguridad: adquisición de imágenes de Windows

En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la adquisición de imágenes de Windows (WIA). En este documento no se proporciona todo lo que necesita saber acerca de los problemas de seguridad; en su lugar, úselo como punto de partida y referencia para esta área tecnológica.

-   [Usar comillas alrededor de los nombres de ruta de acceso](#use-quotation-marks-around-path-names)
-   [Colocar aplicaciones registradas en ubicaciones seguras](#place-registered-applications-in-secure-locations)
-   [No usar directorios subyacentes ni claves del registro](#do-not-use-underlying-directories-or-registry-keys)
-   [Temas relacionados](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Usar comillas alrededor de los nombres de ruta de acceso

Al usar [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar una aplicación para recibir eventos de dispositivo, asegúrese de encerrar la ruta de acceso y el nombre de archivo de la aplicación entre comillas. Esto evita la posibilidad de que la ruta de acceso se interprete erróneamente y se ejecute una aplicación no autorizada.

## <a name="place-registered-applications-in-secure-locations"></a>Colocar aplicaciones registradas en ubicaciones seguras

Cuando una aplicación se registra para recibir un evento de dispositivo, la aplicación puede ejecutarla cualquier usuario que tenga acceso a dicho dispositivo. Por ejemplo, si una aplicación se registra para un evento de análisis, al presionar el botón "examinar" en un escáner se ejecutará la aplicación. Si la aplicación se ejecuta con un privilegio más alto del que tiene el usuario, se produce un posible problema de seguridad.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>No usar directorios subyacentes ni claves del registro

WIA usa varios directorios y claves del registro internamente para almacenar datos o información. No tener acceso directamente a estos directorios o claves del registro. En su lugar, use los métodos de interfaz expuestos para especificar los directorios de las imágenes adquiridas.

## <a name="related-topics"></a>Temas relacionados

-   [Seguridad de Microsoft](https://www.microsoft.com/security/)
-   [Página principal de seguridad de MSDN Library](https://msdn.microsoft.com/security/default.aspx)
-   [Recursos de procedimientos de seguridad](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Recursos de seguridad de TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Consideraciones de seguridad para desarrolladores de Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Prácticas recomendadas de seguridad](../secbp/best-practices-for-the-security-apis.md)

 

 
