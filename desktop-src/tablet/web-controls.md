---
description: Una forma de crear aplicaciones web habilitadas para la entrada de lápiz consiste en colocar Windows Forms controles dentro de awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controles Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705541"
---
# <a name="web-controls"></a>Controles Web

Una forma de crear aplicaciones web habilitadas para la entrada de lápiz consiste en colocar Windows Forms controles dentro de awebpagewithin Microsoft Internet Explorer. Puede encontrar un buen tutorial sobre esta técnica en [uso de Windows Forms controles en Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Los pasos básicos del tutorial son:

1.  Cree un control que herede de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Cree una página HTML con una etiqueta de objeto que haga referencia a ese UserControl.
3.  Cree un directorio virtual y establezca permisos.
4.  Cargue la dirección URL de la página HTML en el explorador.

Esta técnica se puede aplicar a los controles habilitados para tinta, al igual que cualquier otro [**control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms. De hecho, la técnica se puede usar con cualquier clase en el marco de Microsoft .NET. Los ejemplos proporcionados por el kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition incluyen una versión de control Web del ejemplo de notificaciones automáticas en la sección ejemplos de la Web de tinta. En este ejemplo se toma el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md) original y se convierte en un control que se coloca en una página web. Para obtener más información sobre la habilitación de este ejemplo en Web, vea el [ejemplo de control de entrada Web de lápiz](ink-web-control-sample.md).

> [!Note]  
> Cuando se implementa una aplicación creada con .NET a través de la web, la aplicación puede verse afectada por el modelo de seguridad de .NET. Para obtener más información sobre cómo funciona la seguridad con las aplicaciones web habilitadas para tinta, consulte [seguridad y confianza](security-and-trust.md).

 

 

 
