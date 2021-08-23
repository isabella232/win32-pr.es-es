---
title: Compilación del ejemplo Project
description: Compilación del ejemplo Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Reproductor de Windows Media en línea, compilar proyectos de ejemplo
- tiendas en línea, compilar proyectos de ejemplo
- tiendas en línea de tipo 2, compilar proyectos de ejemplo
- Reproductor de Windows Media en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tiendas en línea de tipo 2, proyectos de ejemplo
- Reproductor de Windows Media en línea, asistente para proyectos
- tiendas en línea, asistente para proyectos
- tiendas en línea de tipo 2, asistente para proyectos
- complementos, asistente para proyectos
- Reproductor de Windows Media complementos, asistente para proyectos
- compilar proyectos de ejemplo
- samples,type 2 online stores
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763945"
---
# <a name="compiling-the-sample-project"></a>Compilación del ejemplo Project

El asistente genera todos los archivos que necesita para compilar el proyecto de ejemplo, por lo que no debe tener que cambiar la configuración predeterminada del proyecto. En Visual Studio, en el menú **Compilar** , haga clic en **Compilar solución** para compilar y registrar el componente COM. De forma predeterminada, la configuración de depuración está activa.

> [!Note]  
> En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en Visual Studio nombre o icono y haga clic **en Ejecutar como administrador.**

 

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas Include y Lib donde instaló Windows SDK. El compilador y el vinculador necesitarán acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad Visual Studio Registration que se incluye con el SDK de Windows Vista, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y Lib del SDK de Windows. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el menú **Herramientas** , haga clic en **Opciones**.
2.  Haga **clic en Proyectos y soluciones** y, a continuación, haga clic VC++ **directorios**.
3.  En **Mostrar directorios para**, haga clic en Incluir archivos **o** Archivos **de biblioteca.**
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación del complemento para una tienda en línea de tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




