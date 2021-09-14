---
description: Sensor API proporciona un método que puede usar para solicitar al usuario permisos para usar un sensor o una colección de sensores.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Administración de permisos de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068962"
---
# <a name="managing-user-permissions"></a>Administración de permisos de usuario

Sensor API proporciona un método que puede usar para solicitar al usuario permisos para usar un sensor o una colección de sensores.

Dado que los sensores pueden revelar información confidencial, Windows que los usuarios habiliten sensores antes de que el programa pueda acceder a cualquier dato.

Es posible que quiera solicitar permiso cuando desee usar sensores para los que [**sensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) actual sea SENSOR \_ STATE ACCESS \_ \_ DENIED.

Para solicitar permisos, llame al [**método ISensorManager::RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Al llamar a este método, Windows el **cuadro** de diálogo Habilitar sensores para solicitar al usuario que habilite los sensores solicitados. Este cuadro de diálogo proporciona al usuario los nombres de los sensores solicitados. El usuario puede elegir una de las siguientes opciones:

-   **Habilite estos sensores.**
-   **No habilite estos sensores.**
-   **Abra Panel de control para obtener más opciones.**

Si un usuario elige **No** habilitar estos sensores, Windows  volverá a mostrar el cuadro de diálogo Habilitar sensores para esos sensores concretos, incluso si el programa llama a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Si el usuario elige cualquier otra opción, Windows que se muestre el cuadro de diálogo cuando se solicite. Si la llamada a **RequestPermissions** contiene algunos sensores que el usuario ha elegido mantener deshabilitados previamente, sensor API quitará estos sensores de la lista de sensores que el usuario ve.

### <a name="modal-or-modeless-behavior"></a>Comportamiento modal o no modal

El [**método RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) toma un argumento  **booleano** que determina si el cuadro de diálogo Habilitar sensores se muestra como una ventana modal o no modal. Esta configuración también afecta a si el comportamiento del código de retorno del cuadro de diálogo es sincrónico o asincrónico.

Cuando es modal, el cuadro de diálogo tiene un foco exclusivo entre las ventanas de la aplicación hasta que el usuario elige una opción y el código de retorno **HRESULT** de la llamada a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica la elección del usuario. Cuando se modela, el cuadro de diálogo no tiene un foco exclusivo y la llamada a **RequestPermissions** se devuelve inmediatamente. En este caso, el código de retorno indica si el método se ha correcto, pero no se puede usar para determinar la elección del usuario. A continuación, puede determinar qué sensores se han habilitado controlando el evento [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) y comprobando cada sensor para SENSOR \_ STATE \_ READY.

Para obtener más información sobre los códigos de retorno, vea la [**página de referencia RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Procedimiento recomendado: Evitar varias llamadas modeless a RequestPermissions

Las llamadas modeless repetidas a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) mostrarán varias instancias del cuadro de diálogo Habilitar estos sensores y pueden desbordar la pantalla con cuadros de diálogo, lo que da lugar a una experiencia de usuario deficiente.  Si cree que después de la primera llamada a **RequestPermissions,** podrían instalarse otros sensores de ubicación, que requieren otra llamada a **RequestPermissions,** debe llamar a **RequestPermissions** de forma modal o esperar a que se instalen todos los sensores de ubicación para realizar una llamada modelada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Privacidad y seguridad en la plataforma sensor y ubicación](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Solicitud de permisos de usuario](requesting-user-permissions.md)
</dt> </dl>

 

 
