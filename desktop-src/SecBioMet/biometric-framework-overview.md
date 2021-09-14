---
title: Introducción al marco biométrico
description: La compatibilidad nativa con dispositivos biométricos se incorpora a Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253599"
---
# <a name="biometric-framework-overview"></a>Introducción al marco biométrico

Cada individuo tiene características únicas que se pueden usar para la identificación. Normalmente, estas características son físicas e incluyen rasgos como huellas digitales, pero también pueden incluir rasgos de comportamiento como el acceso y el ritmo de escritura. El término biométrica abarca ambos significados. La información biométrica reemplaza cada vez más las contraseñas para identificar y comprobar a los usuarios. Es más seguro y, a menudo, más cómodo para el usuario y el administrador.

Los sensores se usan para capturar información biométrica. El sensor captura la información como una muestra biométrica. Una sola muestra contiene datos que representan una única característica biométrica para un individuo. Se promedian varios ejemplos para crear una plantilla biométrica y la plantilla se almacena de forma segura. Más adelante, se compara un ejemplo de un usuario desconocido con las plantillas almacenadas para establecer y comprobar la identidad del usuario. El Windows biométrico, que forma parte de Windows Biometric Framework (WBF), proporciona la siguiente funcionalidad. Para aprovechar estas funciones, puede usar la API del Marco biométrico de Windows.

-   Captura muestras biométricas y las usa para crear una plantilla.
-   Guarda y recupera de forma segura las plantillas biométricas.
-   Mapas cada plantilla a un identificador único, como un GUID o SID.

También puede usar esta API para ampliar el marco y crear adaptadores de sensor biométricos, motores correspondientes y componentes de almacenamiento. Para obtener más información sobre cómo crear adaptadores de sensor, motores correspondientes y componentes de almacenamiento, vea [Creating Adapter Plug-ins](creating-adapter-plug-ins.md).

## <a name="core-platform-components"></a>Componentes principales de la plataforma

### <a name="windows-biometric-driver-interface-wbdi"></a>Interfaz de controlador biométrico de Windows (WBDI)

WBDI es una interfaz de programación que un controlador biométrico puede usar para exponer el dispositivo biométrico a través de Windows Biometric Service (WBS). Puede implementar un controlador WBDI mediante cualquier tecnología de controlador compatible, incluido lo siguiente. Sin embargo, se recomienda usar UMDF siempre que sea posible para mejorar la calidad del controlador y la estabilidad del sistema.

-   Marco de controladores en modo de usuario (UMDF)
-   Kernel Mode Driver Framework (KMDF)
-   Windows Modelo de controlador (WDM)

Un controlador biométrico WBDI también debe admitir el GUID de interfaz de controlador WBDI y todos los controles de E/S obligatorios (IOCTL). Los desarrolladores de controladores deben revisar la documentación y el código de ejemplo en Windows Driver Kit (WDK).

### <a name="windows-biometric-service-wbs"></a>Windows Servicio biométrico (WBS)

El Windows Biometric Service administra los controladores biométricos instalados y admite Windows Biometric Framework API para proporcionar acceso a los dispositivos a las aplicaciones cliente. WBS realiza las siguientes funciones:

-   Protege la confidencialidad del usuario separando las aplicaciones cliente de los datos biométricos.
-   Protege los datos biométricos de las aplicaciones cliente sin derechos al exigir que las aplicaciones obtengan acceso a los datos mediante identificadores únicos.
-   Usa un componente de software denominado unidad [biométrica para](/previous-versions//dd401512(v=vs.85)) exponer las funcionalidades de un dispositivo biométrico determinado a través de una interfaz estandarizada.
-   Administra las unidades biométricas agrupandolas en grupos de sensores del sistema, privados o [sinsignar.](sensor-pools.md)
-   Admite el uso de adaptadores de unidad [biométrica](/previous-versions//dd401508(v=vs.85)) para dispositivos físicos que carecen de capacidades de procesamiento o almacenamiento incorporados.

### <a name="windows-biometric-framework-api"></a>API del Marco biométrico de Windows

La API Windows Biometric Framework le permite crear aplicaciones cliente que pueden interactuar con Windows Biometric Service para realizar las siguientes acciones:

-   Identificar y comprobar usuarios.
-   Busque dispositivos biométricos y consulte sus funcionalidades.
-   Administrar sesiones y supervisar eventos.

## <a name="user-experience-components"></a>Componentes de la experiencia del usuario

### <a name="discovery-points"></a>Puntos de detección

Los usuarios finales pueden buscar dispositivos biométricos por cualquiera de los siguientes medios:

-   Escriba las palabras biométrica, huella digital, cara u otras frases relacionadas en el cuadro de texto Iniciar búsqueda para iniciar el panel de control de dispositivos biométricos. La lista de resultados de la biométrica puede contener elementos como los siguientes en una imagen Windows 10 datos.
    -   Configuración del inicio de sesión con huella digital
    -   Configuración del inicio de sesión de face

### <a name="supported-scenarios"></a>Escenarios admitidos

Se admiten los escenarios siguientes:

-   Los usuarios pueden iniciar sesión en un equipo local, en un grupo de trabajo o en un dominio mediante un lector de huellas digitales o una cámara de IR centrada en la cara.
-   Un usuario con privilegios administrativos puede elevar las aplicaciones a través del Control de cuentas de usuario (UAC) mediante una huella digital o una cara.

## <a name="management-components"></a>Componentes de administración

Un sistema biométrico se puede administrar mediante directiva de grupo administración de dispositivos móviles (MDM).

### <a name="biometric-system-management"></a>Administración de sistemas biométricos

Puede administrar funcionalidades biométricas mediante directiva de grupo o MDM. directiva de grupo se puede usar aún más para realizar las siguientes acciones:

-   Especifique el período de tiempo de espera para el cambio rápido de usuarios, si lo implementa el ISV.
-   Impedir la instalación de dispositivos biométricos.
-   Forzar la eliminación de controladores para dispositivos biométricos.
-   Deshabilite el servicio biométrico.

 

 