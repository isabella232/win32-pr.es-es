---
description: En esta sección se describe cómo enviar mensajes desde acciones personalizadas que realmente realizan una parte de la instalación mediante una llamada a una biblioteca de vínculos dinámicos o un script.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Devolver mensajes de error de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c951b0e86d3120b989605572f15681582ac437fca5981852413331a3e63e684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869125"
---
# <a name="returning-error-messages-from-custom-actions"></a>Devolver mensajes de error de acciones personalizadas

En esta sección se describe cómo enviar mensajes desde acciones personalizadas que realmente realizan una parte de la instalación mediante una llamada a una biblioteca de vínculos dinámicos o un script. Tenga en cuenta que El tipo [de acción personalizada 19](custom-action-type-19.md) solo envía un mensaje de error especificado, devuelve un error y, a continuación, finaliza la instalación. El tipo de acción personalizada 19 no realiza ninguna parte de la instalación.

Para enviar un mensaje de error [](dynamic-link-libraries.md) desde una acción personalizada que usa una biblioteca de vínculos dinámicos (DLL), haga que la acción personalizada llame a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Tenga en cuenta que las acciones personalizadas iniciadas por [un control ControlEvent de DoAction](doaction-controlevent.md) pueden enviar mensajes con el [**método Message,**](session-message.md) pero no puede enviar un mensaje **con MsiProcessMessage**. En sistemas anteriores a Windows Server 2003, las acciones personalizadas iniciadas por un control ControlEvent de DoAction no pueden enviar mensajes con el método **MsiProcessMessage** **o Message.** Para obtener más información, vea [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**Para mostrar un mensaje de error desde una acción personalizada mediante un archivo DLL**

1.  La acción personalizada debe llamar [**a MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y pasar los parámetros *hInstall*, *eMessageType* y *hRecord*. El identificador de la instalación, [Custom Action Type 19](custom-action-type-19.md), se puede proporcionar a la acción personalizada como se describe en [Acceso a](accessing-the-current-installer-session-from-inside-a-custom-action.md) la sesión actual del instalador desde dentro de una acción personalizada o desde [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage.**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
2.  El parámetro *eMessageType* debe especificar uno de los tipos de mensaje como se muestra [**en MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).
3.  El *parámetro hRecord* de la [**función MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende del tipo de mensaje. Vea Sending Messages to Windows Installer Using MsiProcessMessage (Envío de mensajes [Windows instalador mediante MsiProcessMessage).](sending-messages-to-windows-installer-using-msiprocessmessage.md) Si el mensaje contiene datos con formato, escriba el mensaje en la [tabla Error](error-table.md) con el formato descrito en [Formato.](formatted.md)

Para enviar un mensaje de error desde una acción personalizada que usa [scripts](scripts.md), la acción personalizada puede llamar al [**método Message**](session-message.md) del [**objeto Session.**](session-object.md)

**Para mostrar un mensaje de error desde una acción personalizada mediante script**

1.  La acción personalizada debe llamar al [**método Message**](session-message.md) del [**objeto Session**](session-object.md) y pasar el tipo de *parámetros y* *registrar*.
2.  El tipo *de parámetro* debe especificar uno de los tipos de mensaje enumerados en el [**método Message.**](session-message.md)
3.  El *parámetro record* del método [**Message**](session-message.md) depende del tipo de mensaje. Si el mensaje contiene datos con formato, escriba el mensaje en la [tabla Error](error-table.md) con el formato descrito en [Formato.](formatted.md)

Las acciones personalizadas que usan [archivos](executable-files.md) ejecutables no pueden enviar un mensaje llamando a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) o al método [**Message**](session-message.md) porque no pueden obtener un identificador para la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Valores devueltos de acción personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



