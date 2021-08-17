---
description: A partir Windows 8, la infraestructura de archivos DLL de AppInit \_ está deshabilitada cuando se habilita el arranque seguro.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: Archivos DLL de AppInit y arranque seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256025"
---
# <a name="appinit-dlls-and-secure-boot"></a>Archivos DLL de AppInit y arranque seguro

A partir Windows 8, la infraestructura de archivos DLL de AppInit \_ está deshabilitada cuando se habilita el arranque seguro.

## <a name="about-appinit_dlls"></a>Acerca de los archivos DLL de AppInit \_

La infraestructura de archivos DLL de AppInit proporciona una manera sencilla de enlazar las API del sistema al permitir que los archivos DLL personalizados se carguen en el espacio de direcciones de \_ cada aplicación interactiva. Tanto las aplicaciones como el software malintencionado usan archivos DLL de AppInit por la misma razón básica, que es enlazar las API; Después de cargar el archivo DLL personalizado, puede enlazar una API del sistema conocida e implementar funcionalidades alternativas. Solo un pequeño conjunto de aplicaciones legítimas modernas usan este mecanismo para cargar archivos DLL, mientras que un gran conjunto de malware usa este mecanismo para poner en peligro los sistemas. Incluso los archivos DLL de AppInit legítimos pueden provocar inintencionalmente interbloqueos del sistema y problemas de rendimiento, por lo que no se recomienda el uso de archivos \_ DLL de \_ AppInit.

## <a name="appinit_dlls-and-secure-boot"></a>Archivos DLL de AppInit \_ y arranque seguro

Windows 8 UEFI y arranque seguro para mejorar la integridad general del sistema y proporcionar una protección sólida frente a amenazas sofisticadas. Cuando se habilita el arranque seguro, el mecanismo de archivos DLL de AppInit se deshabilita como parte de un enfoque sin riesgo para proteger a los clientes frente \_ a malware y amenazas.

Tenga en cuenta que el arranque seguro es un protocolo UEFI y no una Windows 8 segura. Puede encontrar más información sobre UEFI y la especificación del protocolo de arranque seguro en [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>Requisito de certificación de archivos DLL de AppInit \_ Windows 8 aplicaciones de escritorio

Uno de los requisitos de certificación para Windows 8 de escritorio es que la aplicación no debe cargar archivos DLL arbitrarios para interceptar llamadas API win32 mediante el mecanismo de archivos DLL de \_ AppInit. Para obtener información más detallada sobre los requisitos de certificación, consulte la sección 1.1 de Requisitos de certificación para Windows 8 [aplicaciones de escritorio.](../win_cert/certification-requirements-for-windows-desktop-apps.md)

## <a name="summary"></a>Resumen

-   El mecanismo de archivos DLL de AppInit no es un enfoque recomendado para aplicaciones legítimas, ya que puede provocar interbloqueos en el sistema \_ y problemas de rendimiento.
-   El mecanismo de archivos DLL de AppInit \_ está deshabilitado de forma predeterminada cuando se habilita el arranque seguro.
-   El uso de archivos DLL de AppInit \_ en una Windows 8 de escritorio es un error Windows de certificación de aplicaciones de escritorio.

Consulte las siguientes instrucciones para obtener información sobre los archivos DLL de AppInit en Windows 7 y \_ Windows Server 2008 R2: Archivos DLL de AppInit en Windows 7 y [Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
