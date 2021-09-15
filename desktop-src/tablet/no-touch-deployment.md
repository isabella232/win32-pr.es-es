---
description: Microsoft .NET Framework ofrece la capacidad de implementar aplicaciones desde un servidor web o de archivos.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Implementación sin toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579420"
---
# <a name="no-touch-deployment"></a>Implementación sin toque

Microsoft .NET Framework ofrece la capacidad de implementar aplicaciones desde un servidor web o de archivos. Esta técnica, denominada "implementación sin interacción", combina el rendimiento y la interactividad de una aplicación cliente inteligente con todas las ventajas de implementación de una aplicación web. Para implementar la aplicación a través de web, haga clic con el botón derecho en la carpeta que contiene el ejecutable y seleccione **Propiedades.** En la **pestaña Uso compartido** web, seleccione Compartir esta **carpeta.** Escriba un alias para la carpeta. Ahora, el ejecutable se puede ejecutar a través de la Web mediante ese alias como directorio en el servidor. Para obtener más información sobre la implementación sin toque, vea Clientes inteligentes [de .NET](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) e Implementación sin contacto [en el .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Debe tener instalado Microsoft Internet Information Services (IIS) en el equipo para habilitar la pestaña Uso compartido **web** en el cuadro **de diálogo** Propiedades .

 

La implementación sin toque se aplica a las aplicaciones habilitadas para entrada de lápiz de la misma manera que cualquier otra aplicación Windows Forms. Los ejemplos proporcionados por el Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition incluyen una versión de implementación sin toque del ejemplo de notificaciones automáticas, en la sección Ink Web Samples (Ejemplos web de Ink) de los ejemplos. En este ejemplo se toma el [ejemplo de formulario](auto-claims-form-sample.md) de notificaciones automáticas original y se proporciona un instalador que se coloca en un recurso compartido web. Cuando Microsoft Internet Explorer navega a AutoClaims.exe en el directorio que se asigna al recurso compartido web, se inicia la aplicación. Consulte [Ejemplo web de implementación no](no-touch-deployment-web-sample.md) táctil para obtener más información sobre el ejemplo.

> [!Note]  
> Al implementar una aplicación .NET a través de web, el modelo de seguridad de .NET puede afectar a la aplicación. En [la sección Seguridad y confianza](security-and-trust.md) se describe cómo funciona la seguridad con aplicaciones web habilitadas para lápiz.

 

 

 