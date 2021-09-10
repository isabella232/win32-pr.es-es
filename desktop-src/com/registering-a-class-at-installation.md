---
title: Registro de una clase durante la instalación
description: Si una clase está pensada para estar disponible para los clientes en cualquier momento, como la mayoría de las aplicaciones, normalmente se registra a través de un programa de instalación y configuración.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369560"
---
# <a name="registering-a-class-at-installation"></a>Registro de una clase durante la instalación

Si una clase está pensada para estar disponible para los clientes en cualquier momento, como la mayoría de las aplicaciones, normalmente se registra a través de un programa de instalación y configuración. Esto significa colocar información sobre la aplicación en el Registro, incluido cómo y dónde se van a crear instancias de sus objetos. Esta información debe estar registrada para todos los CLID. Otra información es opcional. Herramientas como Regsvr32 hacen que sea fácil escribir un programa de instalación que registre servidores durante la instalación.

Si no confía en los valores predeterminados del sistema, hay dos claves importantes en el Registro: CLSID y AppID. Entre los elementos importantes de información de estas claves se encuentra cómo se va a crear una instancia del objeto. Los objetos se pueden designar como en proceso, fuera de proceso local o fuera de proceso remoto.

En la clave AppID hay varios valores que definen información específica de esa aplicación. Entre ellos se [encuentran RemoteServerName](remoteservername.md) y [ActivateAtStorage,](activateatstorage.md)que se pueden usar para permitir que un cliente cree un objeto, sin que el cliente tenga conocimientos integrados de la ubicación del servidor. (Para obtener más información sobre la creación de instancias remotas, vea [Buscar un objeto](locating-a-remote-object.md) remoto y funciones auxiliares de creación de [instancias).](instance-creation-helper-functions.md)

Un servidor también se puede instalar como un servicio o ejecutarse en una cuenta de usuario específica. Para obtener más información, vea [Installing as a Service Application](installing-as-a-service-application.md).

Un servidor u objeto ROT que no es un servicio o que se ejecuta con una cuenta de usuario específica se puede denominar servidor "activar como activador". Para estos servidores, el contexto de seguridad y la estación de ventana o el escritorio del cliente deben coincidir con el del servidor. Un cliente que intenta conectarse a un servidor remoto se considera que tiene una estación o escritorio de ventana **NULL,** por lo que solo se compara el contexto de seguridad del servidor en esta instancia. (Para obtener más información sobre los SID, vea [Seguridad en COM).](security-in-com.md) COM almacena en caché la estación de ventana o el escritorio de un proceso cuando el proceso se conecta por primera vez al servicio COM distribuido. Por lo tanto, los clientes y servidores COM no deben cambiar su estación de ventana o escritorios de subprocesos del proceso después de llamar a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Cuando una clase se registra como en proceso, COM pasa automáticamente una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) para crear su objeto de clase a la función [**DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) que la clase debe implementar para proporcionar al objeto que realiza la llamada un puntero a su objeto de clase.

Las clases implementadas en ejecutables pueden especificar que COM debe ejecutar su proceso y esperar a que el proceso registre la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) de su objeto de clase a través de una llamada a la [**función CoRegisterClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Claves del Registro COM](com-registry-keys.md)
</dt> <dt>

[Instalación como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registro de un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registrar componentes](registering-components.md)
</dt> <dt>

[Registrar objetos en ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registro propio](self-registration.md)
</dt> </dl>

 

 