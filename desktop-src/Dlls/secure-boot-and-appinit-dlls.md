---
description: A partir de Windows 8, la \_ infraestructura de archivos dll de Appinit está deshabilitada cuando el arranque seguro está habilitado.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: Archivos dll de AppInit y arranque seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688481"
---
# <a name="appinit-dlls-and-secure-boot"></a>Archivos dll de AppInit y arranque seguro

A partir de Windows 8, la \_ infraestructura de archivos dll de Appinit está deshabilitada cuando el arranque seguro está habilitado.

## <a name="about-appinit_dlls"></a>Acerca de los \_ archivos dll de Appinit

La \_ infraestructura de archivos dll de Appinit proporciona una manera sencilla de enlazar las API del sistema al permitir la carga de archivos dll personalizados en el espacio de direcciones de cada aplicación interactiva. Las aplicaciones y el software malintencionado usan archivos dll de AppInit para la misma razón básica, que consiste en enlazar las API; una vez cargado el archivo DLL personalizado, puede enlazar una API del sistema conocida e implementar una funcionalidad alternativa. Solo un pequeño conjunto de aplicaciones legítimas modernas usa este mecanismo para cargar archivos dll, mientras que un gran conjunto de malware usa este mecanismo para poner en peligro los sistemas. Incluso los \_ archivos dll de Appinit legítimos pueden causar involuntariamente interbloqueos del sistema y problemas de rendimiento, por lo que \_ no se recomienda el uso de archivos dll de Appinit.

## <a name="appinit_dlls-and-secure-boot"></a>\_Archivos dll de Appinit y arranque seguro

Windows 8 adoptó UEFI y el arranque seguro para mejorar la integridad global del sistema y proporcionar una protección segura contra amenazas sofisticadas. Cuando el arranque seguro está habilitado, el \_ mecanismo de archivos dll de Appinit está deshabilitado como parte de un enfoque sin compromiso para proteger a los clientes contra malware y amenazas.

Tenga en cuenta que el arranque seguro es un protocolo UEFI y no una característica de Windows 8. Puede encontrar más información sobre UEFI y la especificación del Protocolo de arranque seguro en [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_Requisito de certificación de dll de Appinit para aplicaciones de escritorio de Windows 8

Uno de los requisitos de certificación para aplicaciones de escritorio de Windows 8 es que la aplicación no debe cargar archivos dll arbitrarios para interceptar llamadas a la API de Win32 mediante el \_ mecanismo de archivos dll de Appinit. Para obtener información más detallada sobre los requisitos de certificación, consulte la sección 1,1 de [requisitos de certificación para aplicaciones de escritorio de Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md).

## <a name="summary"></a>Resumen

-   El \_ mecanismo de archivos dll de Appinit no es un enfoque recomendado para aplicaciones legítimas porque puede provocar interbloqueos del sistema y problemas de rendimiento.
-   El \_ mecanismo de archivos dll de Appinit está deshabilitado de forma predeterminada cuando el arranque seguro está habilitado.
-   El uso \_ de archivos dll de Appinit en una aplicación de escritorio de Windows 8 es un error de certificación de la aplicación de escritorio de Windows.

Consulte las siguientes notas del producto para obtener información sobre los \_ archivos dll de Appinit en Windows 7 y Windows server 2008 R2: [AppInit dll en Windows 7 y windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
