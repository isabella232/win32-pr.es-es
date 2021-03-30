---
description: La autenticación está probando quién es.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticación para páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002604"
---
# <a name="authentication-for-web-pages"></a>Autenticación para páginas web

La autenticación está probando quién es.

**Objetivo:** Para que el agente de autenticación web aparezca como parte de la aplicación.

## <a name="prerequisites"></a>Requisitos previos

None

**Tiempo de finalización:** 15 minutos.

## <a name="instructions"></a>Instrucciones

### <a name="1-getting-started"></a>1. Introducción

Inicie el archivo de instalación para instalar un sitio web de Contoso en Internet Information Services 8 en el equipo local para hospedar los archivos HTML y CSS de ejemplo.

1.  Los archivos HTML y CSS de ejemplo se instalarán en el directorio archivos de programa en Microsoft \\ contoso.
2.  Además, una aplicación de la tienda Windows "fabrikam social" se desempaquetará en el escritorio.

### <a name="2-getting-familiar"></a>2. familiarizarse

Para hacerse una idea del aspecto de las páginas de ejemplo en el agente de autenticación Web, abra el archivo de solución Fabrikam social de Visual Studio 11 en la carpeta "fabrikam social" en el escritorio.

1.  Ejecute la aplicación y presione "iniciar" para que aparezcan las páginas de ejemplo en el agente de autenticación Web.
2.  Se puede cambiar el tamaño de la aplicación a un lado o se puede activar compartiendo algunos datos en la aplicación.

### <a name="3-authentication"></a>3. Authentication

Cuando la aplicación subyacente invoca la API de autenticación Web para conectarse al proveedor, "Contoso social", se muestra la página de inicio de sesión. Esta página está diseñada para ser mejor en una experiencia de inicio de sesión rápida y fluida. También proporciona puntos de entrada a algunas otras acciones de usuario comunes, como recuperar detalles de contraseña, registrarse para obtener una cuenta y leer instrucciones sobre la privacidad y los términos y condiciones que se completan en el explorador. ![Página de inicio de sesión de Contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

[Tutorial de resumen para autenticar páginas web](tutorial-for-authenticating-web-pages.md)

Siguiente [autorización para páginas web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
