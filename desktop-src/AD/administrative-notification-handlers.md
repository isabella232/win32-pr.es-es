---
title: Controladores de notificaciones administrativas
description: El complemento MMC de usuarios y equipos de Microsoft Active Directory proporciona un mecanismo para permitir que los componentes reciban notificaciones cuando el usuario elimina, cambia de nombre, mueve o cambia las propiedades de un objeto mediante el complemento.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Controladores de notificación administrativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa6f48f8b56ab8e4a1d64d0fe15543bfee6c09e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904509"
---
# <a name="administrative-notification-handlers"></a>Controladores de notificaciones administrativas

El complemento MMC de usuarios y equipos de Microsoft Active Directory proporciona un mecanismo para permitir que los componentes reciban notificaciones cuando el usuario elimina, cambia de nombre, mueve o cambia las propiedades de un objeto mediante el complemento. El componente que recibe las notificaciones se conoce como "controlador de notificación".

Esto resulta útil cuando se vinculan varios objetos y deben existir en el mismo contenedor. Si se mueve uno de los objetos vinculados, se proporciona una notificación al controlador de notificaciones y el controlador de notificación puede trasladar los demás objetos vinculados a la misma carpeta.

Cuando se realiza una de las operaciones y se instalan uno o varios controladores de notificación, el complemento usuarios y equipos mostrará un cuadro de diálogo de confirmación en el que se muestran los controladores de notificación y una casilla para cada controlador. Si se selecciona la casilla de un controlador, se notifica al controlador. Si la casilla no está activada, no se notifica al controlador.

## <a name="implementing-a-notification-handler"></a>Implementar un controlador de notificación

Un controlador de notificación es un objeto COM implementado como un servidor en proceso. El controlador de notificación debe implementar la interfaz [**IDsAdminNotifyHandler**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler) .

Cuando se produce un evento que producirá una notificación, el complemento usuarios y equipos enumera los controladores de notificaciones registrados y crea cada uno con el CLSID para el controlador. Una vez creado el controlador, el complemento llama al método [**IDsAdminNotifyHandler:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) . El método **Initialize** proporciona el complemento con los eventos que el controlador debe recibir.

Si el evento es uno que se debe enviar al controlador de notificación, el complemento llama al método [**IDsAdminNotifyHandler:: Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) . El método **Begin** proporciona el controlador con el evento que se está produciendo, los datos sobre el objeto en el que se está produciendo el evento y, dependiendo del evento, los datos sobre el objeto que se va a convertir. El método **Begin** también proporciona el complemento con el texto que se debe mostrar para el controlador en el cuadro de diálogo de confirmación.

Cuando se llama al método [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) para cada controlador, el complemento muestra el cuadro de diálogo de confirmación. El cuadro de diálogo de confirmación solicita al usuario que seleccione los controladores que recibirán la notificación. Si el usuario presiona el botón no introducir en el cuadro de diálogo de confirmación, **no** se notificará a ninguno de los controladores. Si el usuario presiona el botón **sí** , cada uno de los controladores seleccionados en el cuadro de diálogo de confirmación recibirá la notificación. El complemento envía la notificación al controlador mediante una llamada al método [**IDsAdminNotifyHandler:: Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) .

Una vez que se ha notificado a todos los controladores, el complemento llama al método [**IDsAdminNotifyHandler:: end**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) . Siempre se llama al método **End** , incluso si no se llama al método [**Notify**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify) .

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registrar un controlador de notificación en el registro de Windows

Al igual que todos los servidores COM, se debe registrar un controlador de notificación en el registro de Windows. El controlador se registra con la clave siguiente:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**<CLSID>** es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . En la **<CLSID>** clave, hay una clave **InProcServer32** que identifica el objeto como servidor de 32 bits en proceso. En la clave **InProcServer32** , la ubicación del archivo dll se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el valor **ThreadingModel** . Todos los controladores de notificación deben usar el modelo de subprocesos de **Apartamento** .

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrar un controlador de notificación con un servidor de Active Directory

Dentro de Active Directory Domain Services, el registro del controlador de notificaciones es específico de una configuración regional. Si el controlador de notificación se aplica a todas las configuraciones regionales, debe registrarse en el objeto **displaySpecifier** en todos los subcontenedores de la configuración regional del contenedor DisplaySpecifiers. Si el controlador de notificación está localizado para una configuración regional determinada, se registra en el objeto **displaySpecifier** en el subcontenedor de la configuración regional. Para obtener más información sobre el contenedor DisplaySpecifiers y las configuraciones regionales, consulte [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).

Los controladores de notificación se registran en el atributo **dsUIAdminNotification** del contenedor **DS-UI-default-Settings** . Este es un valor de cadena Unicode de varios valores, donde cada valor requiere el formato siguiente:


```C++
<order number>,<CLSID>
```



El " &lt; número de pedido &gt; " es un número sin signo que representa la posición del controlador en el cuadro de diálogo de confirmación. Cuando se muestra el cuadro de diálogo de confirmación, los valores se ordenan mediante una comparación de " &lt; número de pedido" de cada valor &gt; . Si hay más de un valor con el mismo " &lt; número de orden &gt; ", esos controladores se muestran en el orden en que se leen en el servidor de Active Directory. Un valor no existente, es decir, uno no utilizado por otros valores de la propiedad, &lt; se debe usar "número de pedido &gt; " si es posible. No hay ninguna posición de inicio prescrita y los huecos pueden aparecer en la &lt; secuencia "número de pedido &gt; ".

" &lt; CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 