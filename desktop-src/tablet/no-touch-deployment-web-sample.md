---
description: En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada en la web mediante una implementación sin interacción.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Ejemplo de Web de implementación de No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104547283"
---
# <a name="no-touch-deployment-web-sample"></a>Ejemplo de Web de implementación de No-Touch

En este ejemplo se muestra cómo implementar una aplicación de Tablet PC administrada en la web mediante una implementación sin interacción. Debe estar familiarizado con los conceptos descritos en [implementación no táctil en el .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp). El equipo debe tener instalado Microsoft Internet Information Services (IIS) para ejecutar este ejemplo.

## <a name="overview"></a>Información general

Con una implementación sin intervención del usuario, las aplicaciones de Windows Forms de Tablet PCWindows se crean mediante las clases del espacio de nombres System. Windows. Forms del marco Microsoft .NET y el kit de desarrollo 1,7 de Microsoft Windows XP Tablet PC Edition, se pueden descargar, instalar y ejecutar directamente en los equipos de los usuarios sin alterar los componentes del registro o del sistema compartido.

Este ejemplo toma el proyecto original para el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md), las notificaciones automáticas y proporciona un proyecto de instalador, autoclaims \_ NoTouchWeb. Una vez compilada y ejecutada, el proyecto del instalador crea una nueva raíz virtual, también denominada autoclaims \_ NoTouchWeb. El instalador copia un archivo, default.htm, que incluye un vínculo al ensamblado de AutoClaims.exe. Para iniciar la aplicación cliente enriquecida, vaya a la raíz virtual con Microsoft Internet Explorer y, a continuación, haga clic en el vínculo de la página default.htm.

> [!Note]  
> Debe desplazarse a la raíz virtual mediante IIS (por ejemplo, https://localhost/AutoClaims\_NoTouchWeb/default.htm) y no directamente a través del sistema de archivos para que la aplicación funcione en el dominio de aplicación de Internet Explorer).

 


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



## <a name="no-touch-deployment-requirements"></a>Requisitos de implementación de No-Touch

Todos los ensamblados dependientes deben encontrarse en la ruta de búsqueda del ensamblado o en la raíz del directorio virtual del sitio Web. El proyecto de implementación de autoclaims \_ NoTouchWeb instala el ensamblado y la página de referencia, default.htm, en la misma raíz virtual (Autoclaims \_ NoTouchWeb).

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.

 

Para obtener más información sobre el uso de entradas manuscritas en la web, consulte [entrada de lápiz en la web](ink-on-the-web.md).

 

 