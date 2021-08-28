---
title: Controladores de notificaciones administrativas
description: El complemento MMC de Microsoft Usuarios y equipos de Active Directory proporciona un mecanismo para permitir que los componentes reciban notificaciones cuando el usuario elimina, cambia el nombre, mueve o cambia las propiedades de un objeto mediante el complemento.
ms.assetid: 49dbb995-c760-4fac-a72f-d5d94afb63c7
ms.tgt_platform: multiple
keywords:
- Controladores de notificaciones administrativas de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d89627cdb15cc7ea15f4b56e3a6ec90eafbe6a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879884"
---
# <a name="administrative-notification-handlers"></a>Controladores de notificaciones administrativas

El complemento MMC de Microsoft Usuarios y equipos de Active Directory proporciona un mecanismo para permitir que los componentes reciban notificaciones cuando el usuario elimina, cambia el nombre, mueve o cambia las propiedades de un objeto mediante el complemento. El componente que recibe las notificaciones se conoce como "controlador de notificaciones".

Esto resulta útil cuando varios objetos están vinculados y deben existir dentro del mismo contenedor. Si se mueve uno de los objetos vinculados, se proporciona una notificación al controlador de notificaciones y el controlador de notificaciones puede mover los demás objetos vinculados a la misma carpeta.

Cuando se realiza una de las operaciones y se instalan uno o varios controladores de notificaciones, el complemento Usuarios y equipos mostrará un cuadro de diálogo de confirmación que enumera los controladores de notificaciones y una casilla para cada controlador. Si se selecciona la casilla de un controlador, se notifica al controlador. Si la casilla no está activada, no se notifica al controlador.

## <a name="implementing-a-notification-handler"></a>Implementar un controlador de notificaciones

Un controlador de notificaciones es un objeto COM implementado como un servidor en proceso. El controlador de notificaciones debe implementar [**la interfaz IDsAdminNotifyHandler.**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnotifyhandler)

Cuando se produce un evento que provocará una notificación, el complemento Usuarios y equipos enumera los controladores de notificaciones registrados y crea cada uno de ellos mediante el CLSID para el controlador. Una vez creado el controlador, el complemento llama al método [**IDsAdminNotifyHandler::Initialize.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-initialize) El **método Initialize** proporciona el complemento con los eventos que el controlador debe recibir.

Si el evento es uno que se debe enviar al controlador de notificaciones, el complemento llama al método [**IDsAdminNotifyHandler::Begin.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) El **método Begin** proporciona al controlador el evento que se está produciendo, los datos sobre el objeto en el que se está produciendo el evento y, en función del evento, los datos sobre lo que se convertirá el objeto. El **método Begin** también proporciona el complemento con el texto que se debe mostrar para el controlador en el cuadro de diálogo de confirmación.

Cuando se ha llamado al método [**Begin**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-begin) para cada controlador, el complemento muestra el cuadro de diálogo de confirmación. El cuadro de diálogo de confirmación solicita al usuario que seleccione qué controladores recibirán la notificación. Si el usuario presiona el botón **No** en el cuadro de diálogo de confirmación, no se notifica a ninguno de los controladores. Si el usuario presiona el botón de inserción **Sí,** cada uno de los controladores seleccionados en el cuadro de diálogo de confirmación recibirá la notificación. El complemento envía la notificación al controlador llamando al método [**IDsAdminNotifyHandler::Notify.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify)

Una vez notificados todos los controladores, el complemento llama al método [**IDsAdminNotifyHandler::End.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-end) Siempre **se** llama al método End, incluso si no se llama al método [**Notify.**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnotifyhandler-notify)

## <a name="registering-a-notification-handler-in-the-windows-registry"></a>Registro de un controlador de notificaciones en Windows Registry

Al igual que todos los servidores COM, se debe registrar un controlador de notificaciones en Windows registro. El controlador se registra con la clave siguiente:


```C++
HKEY_CLASSES_ROOT - CLSID - <CLSID>
```



**&lt; CLSID &gt;** es la representación de cadena del CLSID que genera la [**función StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) En la **&lt; clave &gt; CLSID,** hay una clave **InProcServer32** que identifica el objeto como un servidor en proceso de 32 bits. En la **clave InProcServer32,** la ubicación del archivo DLL se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el valor **ThreadingModel.** Todos los controladores de notificaciones deben usar el **modelo de subprocesamiento** Apartment.

## <a name="registering-a-notification-handler-with-an-active-directory-server"></a>Registrar un controlador de notificaciones con un Active Directory servidor

Dentro Active Directory Domain Services, el registro del controlador de notificaciones es específico de una configuración regional. Si el controlador de notificaciones se aplica a todas las configuraciones regionales, debe registrarse en el objeto **displaySpecifier** en todos los subcontenedores de configuración regional del contenedor DisplaySpecifiers. Si el controlador de notificaciones se localiza para una configuración regional determinada, se registra en el **objeto displaySpecifier** en el subcontenedor de esa configuración regional. Para obtener más información sobre el contenedor DisplaySpecifiers y las configuraciones regionales, vea [Display Specifiers](display-specifiers.md) y [DisplaySpecifiers Container](displayspecifiers-container.md).

Los controladores de notificaciones se registran en el atributo **dsUIAdminNotification** en el **contenedor DS-UI-Default-Configuración.** Se trata de un valor de cadena Unicode multivalor en el que cada valor requiere el formato siguiente:


```C++
<order number>,<CLSID>
```



" order number " es un número sin signo &lt; que representa la posición del controlador en el cuadro de diálogo de &gt; confirmación. Cuando se muestra el cuadro de diálogo de confirmación, los valores se ordenan mediante una comparación del "número &lt; de pedido" de cada &gt; valor. Si más de un valor tiene el mismo " número de pedido ", esos controladores se muestran en el orden en que se leen desde el &lt; &gt; Active Directory servidor. Un no existente, es decir, uno no utilizado por otros valores de la propiedad , " número de pedido " debe &lt; &gt; usarse si es posible. No hay ninguna posición inicial prescrita y pueden aparecer espacios en la secuencia &lt; "número de &gt; pedido".

" CLSID " es la representación de cadena del CLSID tal como la &lt; &gt; genera la función [**StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

 

 
