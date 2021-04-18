---
title: Registrar un servidor EXE en ejecución
description: Registrar un servidor EXE en ejecución
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357499"
---
# <a name="registering-a-running-exe-server"></a>Registrar un servidor EXE en ejecución

Cuando se inicia un servidor ejecutable (EXE), debe llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), que registra el CLSID para el servidor en lo que se denomina la tabla de clases (una tabla diferente de la tabla de objetos en ejecución). Cuando se registra un servidor en la tabla de clases, permite al administrador de control de servicios (SCM) determinar que no es necesario volver a iniciar la clase, porque el servidor ya se está ejecutando. Solo si el servidor no aparece en la lista de clases, el SCM comprobará en el registro los valores adecuados y iniciará el servidor asociado al CLSID dado.

Se pasa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) como CLSID para la clase y un puntero a su interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Los clientes que llaman posteriormente a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con este CLSID recuperarán un puntero a su interfaz solicitada, siempre y cuando la seguridad no lo prohíba. (Consulte [funciones auxiliares de creación de instancias](instance-creation-helper-functions.md) para obtener una descripción de varias funciones de creación y activación de instancias).

El servidor de un objeto de clase debe llamar a [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) para revocar el objeto de clase (quite su registro) cuando se cumplan todas las condiciones siguientes:

-   No hay ninguna instancia existente de la definición del objeto.
-   No hay bloqueos en el objeto de clase.
-   La aplicación que proporciona servicios al objeto de clase no está bajo el control de usuario (no es visible para el usuario en la pantalla).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalar como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registrar una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registrar objetos en la tabla ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 




