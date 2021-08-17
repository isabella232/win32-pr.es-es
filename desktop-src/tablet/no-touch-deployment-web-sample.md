---
description: En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada a través de la Web mediante la implementación sin tocar.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch web de implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449656"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch web de implementación

En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada a través de la Web mediante la implementación sin tocar. Debe estar familiarizado con los conceptos que se deban tratar en Implementación sin contacto [en la .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). El equipo debe tener Microsoft Internet Information Services (IIS) instalado para ejecutar este ejemplo.

## <a name="overview"></a>Información general

Con la implementación sin tocar, las aplicaciones de escritorio de Tablet PCWindows Forms se han creado mediante las clases del sistema. Windows. El espacio de nombres de formularios de Microsoft .NET Framework y microsoft Windows XP Tablet PC Edition Development Kit 1.7 se puede descargar, instalar y ejecutar directamente en los equipos de los usuarios sin que se altere el registro ni los componentes compartidos del sistema.

En este ejemplo se toma el proyecto original de [Ejemplo](auto-claims-form-sample.md)de formulario de notificaciones automáticas, AutoClaims y se proporciona un proyecto de instalador, AutoClaims \_ NoTouchWeb. Una vez compilado y ejecutado, el proyecto de instalador crea una nueva raíz virtual, también denominada AutoClaims \_ NoTouchWeb. El instalador copia un archivo, default.htm, que incluye un vínculo al AutoClaims.exe ensamblado. Para iniciar la aplicación cliente enriquecte, vaya a la raíz virtual con Microsoft Internet Explorer y, a continuación, haga clic en el vínculo de la página default.htm búsqueda.

> [!Note]  
> Debe navegar a la raíz virtual mediante IIS (por ejemplo, y no directamente a través del sistema de archivos para que la aplicación funcione en el dominio Internet Explorer https://localhost/AutoClaims\_NoTouchWeb/default.htm) aplicación.

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>No-Touch de implementación

Todos los ensamblados dependientes deben encontrarse en la ruta de acceso de búsqueda del ensamblado o en la raíz del directorio virtual del sitio web. El proyecto de implementación AutoClaims NoTouchWeb instala el ensamblado y la página de referencia, default.htm, en la misma raíz \_ virtual (AutoClaims \_ NoTouchWeb).

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la subla opción "Ejemplos web compilados previamente" para instalarlos.

 

Para obtener más información sobre el uso de ink en la Web, vea [Ink on the Web](ink-on-the-web.md).

 

 