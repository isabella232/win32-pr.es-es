---
title: Registro de un servidor EXE en ejecución
description: Registro de un servidor EXE en ejecución
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369699"
---
# <a name="registering-a-running-exe-server"></a>Registro de un servidor EXE en ejecución

Cuando se inicia un servidor ejecutable (EXE), debe llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), que registra el CLSID del servidor en lo que se denomina tabla de clases (una tabla diferente de la tabla de objetos en ejecución). Cuando se registra un servidor en la tabla de clases, permite al administrador de control de servicios (SCM) determinar que no es necesario iniciar la clase de nuevo, porque el servidor ya se está ejecutando. Solo si el servidor no aparece en la tabla de clases, el SCM comprobará en el Registro los valores adecuados e iniciará el servidor asociado al CLSID dado.

Se pasa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) el CLSID de la clase y un puntero a su [**interfaz IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Los clientes que posteriormente llaman a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con este CLSID recuperarán un puntero a su interfaz solicitada, siempre que la seguridad no lo prohíba. (Vea [Funciones auxiliares de creación de instancias](instance-creation-helper-functions.md) para obtener una descripción de varias funciones de creación y activación de instancias).

El servidor de un objeto de clase debe llamar a [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) para revocar el objeto de clase (quitar su registro) cuando se cumplen todas las condiciones siguientes:

-   No hay ninguna instancia existente de la definición de objeto.
-   No hay bloqueos en el objeto de clase.
-   La aplicación que proporciona servicios al objeto de clase no está bajo control de usuario (no es visible para el usuario en la pantalla).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalación como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registro de una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registrar objetos en ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro propio](self-registration.md)
</dt> </dl>

 

 




