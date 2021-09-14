---
description: Una manera de crear aplicaciones web habilitadas para lápiz es colocar Windows Forms dentro de awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Controles web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362903"
---
# <a name="web-controls"></a>Controles web

Una manera de crear aplicaciones web habilitadas para lápiz es colocar Windows Forms dentro de awebpagewithin Microsoft Internet Explorer. Puede encontrar un buen tutorial sobre esta técnica en [Using Windows Forms Controls in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Los pasos básicos del tutorial son:

1.  Cree un control que herede de [**System.Windows. Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Cree una página HTML con una etiqueta de objeto que haga referencia a ese UserControl.
3.  Cree un directorio virtual y establezca los permisos.
4.  Cargue la dirección URL de la página HTML en el explorador.

Esta técnica se puede aplicar a controles habilitados para entrada de lápiz, al igual que cualquier otro control Windows Forms [**Control**](/dotnet/api/system.windows.forms.control?view=netcore-3.1). De hecho, la técnica se puede usar con cualquier clase de microsoft .NET Framework. Los ejemplos proporcionados por el Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition incluyen una versión de control web del ejemplo de notificaciones automáticas en la sección Ink Web Samples (Ejemplos web de Ink). En este ejemplo se toma el [ejemplo de formulario](auto-claims-form-sample.md) de notificaciones automáticas original y se convierte en un control que se coloca en una página web. Para obtener más información sobre la habilitación web de este ejemplo, vea El ejemplo [de control web ink](ink-web-control-sample.md).

> [!Note]  
> Al implementar una aplicación creada mediante .NET a través de la Web, el modelo de seguridad para .NET puede afectar a la aplicación. Para obtener más información sobre cómo funciona la seguridad con aplicaciones web habilitadas para lápiz, vea [Seguridad y confianza.](security-and-trust.md)

 

 

 
