---
description: La autorización establece a qué recursos tiene acceso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorización para páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141337"
---
# <a name="authorization-for-web-pages"></a>Autorización para páginas web

La autorización establece a qué recursos tiene acceso.

**Objetivo:** Para permitir que los usuarios accedan a la aplicación.

## <a name="prerequisites"></a>Requisitos previos

Ninguno

**Tiempo para completar:** 2 minutos.

## <a name="instructions"></a>Instructions

### <a name="1-authorization"></a>1. Autorización

Cuando el usuario escribe sus credenciales y hace clic en el botón Inicio de sesión, se muestra la página de permisos. Esta página es mejor para permitir que los usuarios controle permisos pormenorizados al conceder a la aplicación acceso a los datos de Contoso. ![página de permisos de contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Uso del ejemplo

Debe conocer los siguientes archivos HTML y CSS.

1.  Los siguientes archivos HTML corresponden a las dos páginas del flujo de autorización web
    -   WebAuthLogin.html: HTML de ejemplo para la página de inicio de sesión
    -   WebAuthPermissions.html: HTML de ejemplo para la página de permisos
2.  Los archivos CSS contienen estilos Windows 8 para ayudar a crear una Windows web de la aplicación store.
    -   ui-light.css: se ha derivado de la hoja de estilos base para Windows 8 controles.
    -   ui-webauth.css: proporciona un estilo incremental para optimizar el diseño de las páginas de autenticación web.
    -   theme-colors.css: proporciona el estilo incremental para invalidar los colores de acentos predeterminados de los controles con el color de marca del proveedor.

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Tutorial de [resumen para autenticar páginas web](tutorial-for-authenticating-web-pages.md)

Procedimientos [recomendados siguientes para diseñar páginas web de autenticación](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consideraciones para el desarrollo de páginas web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicación de ejemplo del SDK del Agente de autenticación web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
