---
description: Un paquete de instalación contiene toda la información que el instalador de Windows requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Paquete de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633825"
---
# <a name="installation-package"></a>Paquete de instalación

Un paquete de instalación contiene toda la información que el instalador de Windows requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación. Cada paquete de instalación incluye un .msi de instalación, que contiene una base de datos de instalación, un flujo de información de resumen y flujos de datos para varias partes de la instalación. El .msi archivo también puede contener una o varias transformaciones, archivos de código fuente internos y archivos de código fuente externos o archivos archivadores necesarios para la instalación.

Los desarrolladores de aplicaciones deben crear una instalación para usar el instalador. Dado que el instalador organiza las instalaciones en torno al concepto de componentes y características [,](components-and-features.md)y almacena toda la información sobre la instalación en una base de datos relacional, el proceso de creación de un paquete de instalación conlleva ampliamente los pasos siguientes:

-   Identifique las características que se presentarán a los usuarios.
-   Organice la aplicación en componentes.
-   Rellene la base de datos de instalación con información.
-   Valide el paquete de instalación.

En la sección siguiente se deba a los componentes y características del instalador. Para obtener más información, vea [Componentes y características.](components-and-features.md) La elección de características normalmente viene determinada por la funcionalidad de la aplicación desde la perspectiva del usuario.

Se recomienda que los desarrolladores usen un procedimiento estándar para elegir componentes. Para obtener más información, vea [Organización de aplicaciones en componentes](organizing-applications-into-components.md).

Los autores de paquetes pueden usar herramientas de creación de paquetes de terceros, o un editor de tablas y el SDK Windows Installer, para rellenar la base de datos de instalación. Todos los paquetes de instalación deben validarse para mantener la coherencia interna. Para obtener más información, vea [Validación de paquetes.](package-validation.md)

 

 



