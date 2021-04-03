---
description: La autorización establece los recursos a los que tiene acceso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorización para páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908433"
---
# <a name="authorization-for-web-pages"></a>Autorización para páginas web

La autorización establece los recursos a los que tiene acceso.

**Objetivo:** Para permitir que los usuarios accedan a la aplicación.

## <a name="prerequisites"></a>Requisitos previos

None

**Tiempo de finalización:** 2 minutos.

## <a name="instructions"></a>Instrucciones

### <a name="1-authorization"></a>1. autorización

Cuando el usuario escribe sus credenciales y hace clic en el botón de inicio de sesión, se muestra la página permisos. Esta página es la mejor opción para permitir que los usuarios controlen los permisos granulares para conceder a la aplicación acceso a los datos de contoso. ![Página permisos de Contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Cómo utilizar el ejemplo

Debe conocer los siguientes archivos HTML y CSS.

1.  Los siguientes archivos HTML se corresponden con las dos páginas del flujo de autorización Web
    -   WebAuthLogin.html: código HTML de ejemplo para la página de inicio de sesión
    -   WebAuthPermissions.html: HTML de ejemplo de la página de permisos
2.  Los archivos CSS contienen estilos de Windows 8 para ayudar a crear una página web de la aplicación de la tienda Windows.
    -   UI-Light. CSS: se ha derivado de la hoja de estilos base para los controles de Windows 8.
    -   UI-webauth. CSS: proporciona un estilo incremental para optimizar el diseño de las páginas de autenticación Web.
    -   Theme-colors. CSS: proporciona el estilo incremental para invalidar los colores de énfasis predeterminados de los controles con el color de la marca del proveedor.

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

[Tutorial de resumen para autenticar páginas web](tutorial-for-authenticating-web-pages.md)

Siguientes [prácticas recomendadas para diseñar páginas web de autenticación](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
