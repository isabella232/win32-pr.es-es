---
description: Un paquete de instalación contiene toda la información que el Windows Installer requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Paquete de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652745"
---
# <a name="installation-package"></a>Paquete de instalación

Un paquete de instalación contiene toda la información que el Windows Installer requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación. Cada paquete de instalación incluye un archivo. msi que contiene una base de datos de instalación, un flujo de información de Resumen y secuencias de datos para varias partes de la instalación. El archivo. msi también puede contener una o más transformaciones, archivos de código fuente internos y archivos de código fuente externos o archivos. cab necesarios para la instalación.

Los desarrolladores de aplicaciones deben crear una instalación para usar el instalador. Dado que el instalador organiza las instalaciones en torno al concepto de [componentes y características](components-and-features.md), y almacena toda la información sobre la instalación en una base de datos relacional, el proceso de creación de un paquete de instalación conlleva en general los siguientes pasos:

-   Identifique las características que se van a presentar a los usuarios.
-   Organice la aplicación en componentes.
-   Rellene la base de datos de instalación con información.
-   Valide el paquete de instalación.

En la siguiente sección se describen los componentes y las características del instalador. Para obtener más información, vea [componentes y características](components-and-features.md). La elección de las características viene determinada normalmente por la funcionalidad de la aplicación desde la perspectiva del usuario.

Se recomienda que los desarrolladores utilicen un procedimiento estándar para elegir componentes. Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).

Los autores de paquetes pueden usar herramientas de creación de paquetes de terceros, o un editor de tablas y el SDK de Windows Installer, para rellenar la base de datos de instalación. Todos los paquetes de instalación deben validarse para la coherencia interna. Para obtener más información, vea [validación de paquetes](package-validation.md).

 

 



