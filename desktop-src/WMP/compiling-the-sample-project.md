---
title: Compilar el proyecto de ejemplo
description: Compilar el proyecto de ejemplo
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player tiendas en línea, compilar proyectos de ejemplo
- tiendas en línea, compilar proyectos de ejemplo
- tipo 2 tiendas en línea, compilar proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- Windows Media Player tiendas en línea, Asistente para proyectos
- tiendas en línea, Asistente para proyectos
- tipo 2 tiendas en línea, Asistente para proyectos
- complementos, Asistente para proyectos
- Complementos de Windows Media Player, Asistente para proyectos
- compilar proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695369"
---
# <a name="compiling-the-sample-project"></a>Compilar el proyecto de ejemplo

El asistente genera todos los archivos que necesita para compilar el proyecto de ejemplo, por lo que no debe cambiar la configuración predeterminada del proyecto. En Visual Studio, en el menú **compilar** , haga clic en **compilar solución** para compilar y registrar el componente com. De forma predeterminada, la configuración de depuración está activa.

> [!Note]  
> En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo. Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.

 

Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK. El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.

Si ejecutó la utilidad de registro de Visual Studio que se incluye con el SDK de Windows Vista, es probable que el entorno de desarrollo ya se haya configurado para que apunte al Windows SDK carpetas include y lib. De lo contrario, debe configurar manualmente el entorno de desarrollo.

Para configurar manualmente Visual Studio, siga estos pasos.

1.  En el menú **Herramientas** , haga clic en **Opciones**.
2.  Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.
3.  En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.
4.  Agregue los directorios de los archivos necesarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar el complemento para una tienda en línea de tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




