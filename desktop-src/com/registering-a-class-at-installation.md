---
title: Registrar una clase durante la instalación
description: Si una clase está pensada para estar disponible para los clientes en cualquier momento, como la mayoría de las aplicaciones, normalmente la registra a través de un programa de instalación y configuración.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359446"
---
# <a name="registering-a-class-at-installation"></a>Registrar una clase durante la instalación

Si una clase está pensada para estar disponible para los clientes en cualquier momento, como la mayoría de las aplicaciones, normalmente la registra a través de un programa de instalación y configuración. Esto significa incluir información sobre la aplicación en el registro, lo que incluye cómo y dónde se crearán instancias de sus objetos. Esta información debe registrarse para todos los CLSID. Otra información es opcional. Las herramientas como regsvr32 facilitan la escritura de un programa de instalación que registra los servidores durante la instalación.

Si no se basa en los valores predeterminados del sistema, hay dos claves importantes en el registro: el CLSID y el AppID. Entre las partes importantes de la información que se encuentran en estas claves, se explica cómo se crea una instancia del objeto. Los objetos se pueden designar como en proceso, locales fuera de proceso o remotos fuera de proceso.

En la clave AppID hay varios valores que definen la información específica de esa aplicación. Entre ellas se encuentran [RemoteServerName](remoteservername.md) y [ActivateAtStorage](activateatstorage.md), que se pueden usar para permitir a un cliente crear un objeto, con el cliente sin conocimiento integrado de la ubicación del servidor. (Para obtener más información acerca de la creación de instancias remotas, vea [localizar un objeto remoto](locating-a-remote-object.md) y [funciones auxiliares](instance-creation-helper-functions.md)para la creación de instancias).

Un servidor también se puede instalar como un servicio o para ejecutarse en una cuenta de usuario específica. Para obtener más información, vea [instalar como aplicación de servicio](installing-as-a-service-application.md).

Un servidor o un objeto ROT que no sea un servicio o que se ejecute en una cuenta de usuario específica se puede denominar servidor "activar como activador". Para estos servidores, el contexto de seguridad y la estación de ventana/escritorio del cliente deben coincidir con los del servidor. Un cliente que intenta conectarse a un servidor remoto se considera que tiene un escritorio o estación de ventana **null** , por lo que solo se compara el contexto de seguridad del servidor en esta instancia. (Para obtener más información acerca de los SID, vea [seguridad en com](security-in-com.md)). COM almacena en caché la estación de ventana o el escritorio de un proceso cuando el proceso se conecta por primera vez al servicio COM distribuido. Por lo tanto, los clientes y servidores COM no deben cambiar su estación de ventana o escritorios de subprocesos del proceso después de llamar a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Cuando una clase se registra como in-Process, COM pasa automáticamente una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) para crear su objeto de clase a la función [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , que la clase debe implementar para dar al objeto que realiza la llamada un puntero a su objeto de clase.

Las clases implementadas en archivos ejecutables pueden especificar que COM debe ejecutar su proceso y esperar a que el proceso registre la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) del objeto de clase a través de una llamada a la función [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del registro COM](com-registry-keys.md)
</dt> <dt>

[Instalar como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registrar un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar componentes](registering-components.md)
</dt> <dt>

[Registrar objetos en la tabla ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 