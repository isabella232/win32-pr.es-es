---
description: La autenticación está demostrando quién es.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticación para páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46a063cdd63631f84aa21980f89a143b3d1e9b42af020799d0f9f1bb7502b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141447"
---
# <a name="authentication-for-web-pages"></a>Autenticación para páginas web

La autenticación está demostrando quién es.

**Objetivo:** Para que el agente de autenticación web aparezca como parte de la aplicación.

## <a name="prerequisites"></a>Requisitos previos

Ninguno

**Tiempo de ejecución:** 15 minutos.

## <a name="instructions"></a>Instructions

### <a name="1-getting-started"></a>1. Introducción

Inicie el archivo de instalación para instalar un sitio web de Contoso en Internet Information Services 8 en el equipo local para hospedar los archivos HTML y CSS de ejemplo.

1.  Los archivos HTML y CSS de ejemplo se instalarán en el directorio de archivos de programa en Microsoft \\ Contoso.
2.  Además, una aplicación "Fabrikam Social" Windows Store se desempaquete en el escritorio.

### <a name="2-getting-familiar"></a>2. Familiarización

Para ver el aspecto de las páginas de ejemplo en el Agente de autenticación web, abra el archivo de solución Fabrikam Social Visual Studio 11 en la carpeta "Fabrikam Social" del escritorio.

1.  Ejecute la aplicación y presione "Iniciar" para abrir las páginas de ejemplo en el Agente de autenticación web.
2.  La aplicación se puede cambiar de tamaño a un lado o activarse compartiendo algunos datos con la aplicación.

### <a name="3-authentication"></a>3. Authentication

Cuando la aplicación subyacente invoca la API de autenticación web para conectarse al proveedor, "Contoso Social", se muestra la página de inicio de sesión. Esta página está diseñada para ser la mejor en una experiencia de inicio de sesión rápida y fluida. También proporciona puntos de entrada a otras acciones comunes del usuario, como recuperar detalles de contraseña, registrarse para obtener una cuenta y leer instrucciones sobre privacidad y términos y condiciones que se completan en el explorador. ![página de inicio de sesión de contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Tutorial de [resumen para autenticar páginas web](tutorial-for-authenticating-web-pages.md)

Siguiente [autorización para páginas web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
