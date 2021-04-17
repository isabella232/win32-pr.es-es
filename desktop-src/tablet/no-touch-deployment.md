---
description: El marco de Microsoft .NET proporciona la capacidad de implementar aplicaciones desde un servidor web o de archivos.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Sin implementación táctil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105717333"
---
# <a name="no-touch-deployment"></a>Sin implementación táctil

El marco de Microsoft .NET proporciona la capacidad de implementar aplicaciones desde un servidor web o de archivos. Esta técnica, denominada "implementación no táctil", combina el rendimiento y la interactividad de una aplicación cliente inteligente con todas las ventajas de implementación de una aplicación Web. Para implementar la aplicación en la web, haga clic con el botón derecho en la carpeta que contiene el ejecutable y seleccione **propiedades**. En la pestaña **uso compartido de web** , seleccione **compartir esta carpeta**. Escriba un alias para la carpeta. Ahora, el archivo ejecutable se puede ejecutar a través de la web mediante ese alias como directorio del servidor. Para obtener más información sobre la implementación no táctil, vea [.net Smart clients](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) y [no-Touch deployment en el .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Debe tener Microsoft Internet Information Services (IIS) instalado en el equipo para habilitar la ficha **uso compartido de web** en el cuadro de diálogo **propiedades** .

 

La implementación no táctil se aplica a las aplicaciones habilitadas para tinta de la misma manera que cualquier otra aplicación Windows Forms. Los ejemplos proporcionados por el kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition incluyen una versión de implementación no táctil del ejemplo de notificaciones automáticas, en la sección ejemplos de tintas Web de los ejemplos. En este ejemplo se toma el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md) original y se proporciona un instalador que coloca en un recurso compartido de Web. Cuando Microsoft Internet Explorer navega a AutoClaims.exe en el directorio que se asigna al recurso compartido Web, se inicia la aplicación. Para obtener más información sobre el ejemplo [, consulte ejemplo de Web de implementación sin interacción](no-touch-deployment-web-sample.md) .

> [!Note]  
> Al implementar una aplicación .NET a través de la web, la aplicación puede verse afectada por el modelo de seguridad de .NET. En la sección [seguridad y confianza](security-and-trust.md) se describe cómo funciona la seguridad con las aplicaciones web habilitadas para tinta.

 

 

 