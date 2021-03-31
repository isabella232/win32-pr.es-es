---
description: En esta sección se describe cómo enviar mensajes de acciones personalizadas que realmente realizan una parte de la instalación mediante una llamada a una biblioteca de vínculos dinámicos o un script.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Devolver mensajes de error de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480a9e7891680aadc9d8eb4eedba2bad0d2e3dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155516"
---
# <a name="returning-error-messages-from-custom-actions"></a>Devolver mensajes de error de acciones personalizadas

En esta sección se describe cómo enviar mensajes de acciones personalizadas que realmente realizan una parte de la instalación mediante una llamada a una biblioteca de vínculos dinámicos o un script. Tenga en cuenta que el [tipo de acción personalizada 19](custom-action-type-19.md) solo envía un mensaje de error especificado, devuelve un error y, a continuación, finaliza la instalación. El tipo de acción personalizada 19 no realiza ninguna parte de la instalación.

Para enviar un mensaje de error desde una acción personalizada que usa una [biblioteca de vínculos dinámicos](dynamic-link-libraries.md) (dll), haga que la acción personalizada llame a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Tenga en cuenta que las acciones personalizadas iniciadas por una [ControlEvent, de acción](doaction-controlevent.md) pueden enviar mensajes con el método de [**mensaje**](session-message.md) , pero no pueden enviar un mensaje con **MsiProcessMessage**. En sistemas anteriores a Windows Server 2003, las acciones personalizadas iniciadas por una acción ControlEvent, no pueden enviar mensajes con **MsiProcessMessage** o un método de **mensaje** . Para obtener más información, consulte [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**Para mostrar un mensaje de error desde una acción personalizada mediante un archivo DLL**

1.  La acción personalizada debe llamar a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y pasar los parámetros *hInstall*, *eMessageType* y *hRecord*. El identificador de la instalación, el [tipo de acción personalizada 19](custom-action-type-19.md), se puede proporcionar a la acción personalizada, como se describe en [obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md) o desde [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea).
2.  El parámetro *eMessageType* debe especificar uno de los tipos de mensaje, tal y como se muestra en [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).
3.  El parámetro *hRecord* de la función [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende del tipo de mensaje. Consulte [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md). Si el mensaje contiene datos con formato, escriba el mensaje en la tabla de [errores](error-table.md) con el formato descrito en [con formato](formatted.md).

Para enviar un mensaje de error desde una acción personalizada que usa [scripts](scripts.md), la acción personalizada puede llamar al método de [**mensaje**](session-message.md) del objeto de [**sesión**](session-object.md) .

**Para mostrar un mensaje de error desde una acción personalizada mediante un script**

1.  La acción personalizada debe llamar al método de [**mensaje**](session-message.md) del objeto de [**sesión**](session-object.md) y pasar el *tipo* y el *registro* de los parámetros.
2.  El *tipo* de parámetro debe especificar uno de los tipos de mensaje que aparecen en el método de [**mensaje**](session-message.md) .
3.  El parámetro de *registro* del método de [**mensaje**](session-message.md) depende del tipo de mensaje. Si el mensaje contiene datos con formato, escriba el mensaje en la tabla de [errores](error-table.md) con el formato descrito en [con formato](formatted.md).

Las acciones personalizadas que utilizan [archivos ejecutables](executable-files.md) no pueden enviar un mensaje mediante una llamada a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) o el método de [**mensaje**](session-message.md) porque no pueden obtener un identificador para la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Valores devueltos de la acción personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



