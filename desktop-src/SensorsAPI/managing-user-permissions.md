---
description: La API de sensor proporciona un método que puede usar para pedir al usuario permisos para usar un sensor o una colección de sensores.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Administrar permisos de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001037"
---
# <a name="managing-user-permissions"></a>Administrar permisos de usuario

La API de sensor proporciona un método que puede usar para pedir al usuario permisos para usar un sensor o una colección de sensores.

Dado que los sensores pueden revelar información confidencial, Windows requiere que los usuarios habiliten los sensores antes de que el programa pueda acceder a los datos.

Es posible que desee solicitar permiso cuando desee usar sensores para los que el [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) actual es \_ \_ acceso denegado al estado del sensor \_ .

Para solicitar permisos, llame al método [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) . Cuando se llama a este método, Windows abre el cuadro de diálogo **Habilitar sensores** para solicitar al usuario que habilite los sensores solicitados. Este cuadro de diálogo proporciona al usuario los nombres de los sensores solicitados. El usuario puede elegir una de las siguientes opciones:

-   **Habilite estos sensores**.
-   **No habilite estos sensores**.
-   **Abra el panel de control para obtener más opciones**.

Si un usuario elige **no habilitar estos sensores**, Windows no volverá a mostrar el cuadro de diálogo **Habilitar sensores** para esos sensores determinados, incluso si el programa llama a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Si el usuario elige cualquier otra opción, Windows permitirá que se muestre el cuadro de diálogo cuando se solicite. Si la llamada a **RequestPermissions** contiene algunos sensores que el usuario ha elegido previamente para mantener deshabilitado, la API de sensor quitará estos sensores de la lista de sensores que ve el usuario.

### <a name="modal-or-modeless-behavior"></a>Comportamiento modal o no modal

El método [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) toma un argumento **booleano** que determina si el cuadro de diálogo **Habilitar sensores** se muestra como una ventana modal o no modal. Esta configuración también afecta a si el comportamiento del código de retorno del cuadro de diálogo es sincrónico o asincrónico.

Cuando es modal, el cuadro de diálogo tiene el foco exclusivo entre las ventanas de la aplicación hasta que el usuario elige una opción y el código de retorno **HRESULT** de la llamada a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica la elección del usuario. Cuando el modelo no es modal, el cuadro de diálogo no tiene el foco exclusivo y la llamada a **RequestPermissions** se devuelve inmediatamente. En este caso, el código de retorno indica si el método se realizó correctamente, pero no se puede usar para determinar la elección del usuario. A continuación, puede determinar qué sensores se han habilitado controlando el evento [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) y seleccionando cada sensor para estado de sensor \_ \_ preparado.

Para obtener más información sobre los códigos de retorno, vea la página de referencia de [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) .

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Procedimiento recomendado: evitar varias llamadas no modales a RequestPermissions

Las llamadas no modales repetidas a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) mostrarán varias instancias del cuadro de diálogo **Habilitar estos sensores** y pueden inundar la pantalla con cuadros de diálogo, lo que produce una mala experiencia de usuario. Si cree que, después de la primera llamada a **RequestPermissions**, es posible que se instalen otros sensores de ubicación, lo que requiere otra llamada a **RequestPermissions**, debe llamar a **RequestPermissions** de forma modal o esperar hasta que se instalen todos los sensores de ubicación para realizar una llamada no modal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Privacidad y seguridad en la plataforma de sensor y ubicación](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Solicitar permisos de usuario](requesting-user-permissions.md)
</dt> </dl>

 

 
