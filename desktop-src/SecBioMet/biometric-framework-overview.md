---
title: Información general sobre el marco biométrico
description: La compatibilidad nativa con dispositivos biométricos se incorpora en Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488019"
---
# <a name="biometric-framework-overview"></a>Información general sobre el marco biométrico

Cada individuo tiene características únicas que se pueden usar para la identificación. Normalmente, estas características son físicas e incluyen rasgos como las huellas digitales, pero también pueden incluir rasgos de comportamiento, como el y ritmo de escritura. El término biometría engloba ambos significados. La información biométrica reemplaza constantemente las contraseñas para identificar y comprobar a los usuarios. Es más seguro y suele ser más conveniente para el usuario y el administrador.

Los sensores se usan para capturar información biométrica. El sensor captura la información como un ejemplo biométrico. Un único ejemplo contiene datos que representan una única característica biométrica para un individuo. Se calcula el promedio de varios ejemplos para crear una plantilla biométrica y la plantilla se almacena de forma segura. Más adelante, se comparará un ejemplo de un usuario desconocido con las plantillas almacenadas para establecer y comprobar la identidad del usuario. El servicio biométrico de Windows, que forma parte del Plataforma de biometría de Windows (WBF), proporciona la siguiente funcionalidad. Para aprovechar estas funciones, puede usar la API del Marco biométrico de Windows.

-   Captura muestras biométricas y las usa para crear una plantilla.
-   Guarda y recupera de forma segura plantillas biométricas.
-   Asigna cada plantilla a un identificador único, como un GUID o SID.

También puede usar esta API para ampliar el marco de trabajo y crear adaptadores de sensor biométricos, motores de coincidencia y componentes de almacenamiento. Para obtener más información acerca de la creación de adaptadores de sensores, motores de coincidencia y componentes de almacenamiento, consulte [crear complementos de adaptador](creating-adapter-plug-ins.md).

## <a name="core-platform-components"></a>Componentes principales de la plataforma

### <a name="windows-biometric-driver-interface-wbdi"></a>Interfaz de controlador biométrico de Windows (WBDI)

WBDI es una interfaz de programación que un controlador biométrico puede usar para exponer el dispositivo biométrico a través del servicio biométrico de Windows (WBS). Puede implementar un controlador de WBDI con cualquier tecnología de controladores admitida, como la siguiente. No obstante, se recomienda usar UMDF cuando sea posible para mejorar la calidad del controlador y la estabilidad del sistema.

-   Marco de trabajo de controlador de modo de usuario (UMDF)
-   Marco de controlador de modo kernel (KMDF)
-   Modelo de controlador de Windows (WDM)

Un controlador biométrico de WBDI también debe admitir el GUID de la interfaz del controlador de WBDI y todos los controles de e/s obligatorios (ioctl). Los desarrolladores de controladores deben revisar la documentación y el código de ejemplo en el kit de controladores de Windows (WDK).

### <a name="windows-biometric-service-wbs"></a>Servicio biométrico de Windows (WBS)

El servicio biométrico de Windows administra los controladores biométricos instalados y admite el Plataforma de biometría de Windows API para proporcionar acceso al dispositivo a las aplicaciones cliente. WBS realiza las siguientes funciones:

-   Protege la confidencialidad del usuario al separar las aplicaciones cliente de datos biométricos.
-   Protege los datos biométricos de las aplicaciones cliente sin privilegios, ya que requiere que las aplicaciones obtengan acceso a los datos mediante identificadores únicos.
-   Usa un componente de software denominado [unidad biométrica](/previous-versions//dd401512(v=vs.85)) para exponer las capacidades de un dispositivo biométrico determinado a través de una interfaz normalizada.
-   Administra las unidades biométricas mediante su agrupación en [grupos de sensores](sensor-pools.md)del sistema, privados o sin asignar.
-   Admite el uso de [adaptadores](/previous-versions//dd401508(v=vs.85)) de unidad biométricos para dispositivos físicos que carecen de capacidades de almacenamiento o procesamiento incorporadas.

### <a name="windows-biometric-framework-api"></a>API del Marco biométrico de Windows

La API de Plataforma de biometría de Windows permite crear aplicaciones cliente que pueden interactuar con el servicio biométrico de Windows para realizar las siguientes acciones:

-   Identifique y compruebe los usuarios.
-   Busque dispositivos biométricos y consulte sus capacidades.
-   Administrar sesiones y supervisar eventos.

## <a name="user-experience-components"></a>Componentes de experiencia del usuario

### <a name="discovery-points"></a>Puntos de detección

Los usuarios finales pueden buscar dispositivos biométricos mediante cualquiera de los siguientes medios:

-   Escribir las palabras biometría, huella digital, esfera u otras frases relacionadas en el cuadro de texto Iniciar búsqueda para iniciar el panel de control de dispositivos biométricos. La lista de resultados para biometría puede contener elementos como los siguientes en una imagen de Windows 10.
    -   Configuración del inicio de sesión con huella digital
    -   Configuración del inicio de sesión facial

### <a name="supported-scenarios"></a>Escenarios admitidos

Se admiten los escenarios siguientes:

-   Los usuarios pueden iniciar sesión en un equipo local, un grupo de trabajo o en un dominio mediante un lector de huellas digitales o una cámara de INFRARROJOs centrada en la superficie.
-   Un usuario con privilegios de administrador puede elevar las aplicaciones a través del control de cuentas de usuario (UAC) mediante una huella digital o una superficie.

## <a name="management-components"></a>Componentes de administración

Un sistema biométrico se puede administrar mediante directiva de grupo o la administración de dispositivos móviles (MDM).

### <a name="biometric-system-management"></a>Administración de sistemas biométricos

Puede administrar las capacidades biométricas mediante directiva de grupo o MDM. Directiva de grupo se puede usar para realizar las siguientes acciones:

-   Especifique el período de tiempo de espera para el cambio rápido de usuario, si lo ha implementado el ISV.
-   Evitar la instalación de dispositivos biométricos.
-   Fuerce la eliminación de controladores para dispositivos biométricos.
-   Deshabilite el servicio biométrico.

 

 