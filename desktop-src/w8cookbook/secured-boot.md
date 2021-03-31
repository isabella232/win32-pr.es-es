---
title: Antimalware de inicio temprano
description: Antimalware de inicio temprano
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104083520"
---
# <a name="early-launch-antimalware"></a>Antimalware de inicio temprano

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  

## <a name="description"></a>Descripción

A medida que el software antimalware (AM) es mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también se están volviendo mejor en la creación de rootkits que pueden ocultarse de la detección. La detección de malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM se direccionan diligentemente. Normalmente, crean hackers del sistema que no son compatibles con el sistema operativo host y, en realidad, pueden poner el equipo en un estado inestable. Hasta este punto, Windows no ha proporcionado una buena forma de que AM detecte y resuelva estas amenazas de arranque iniciales.

Windows 8 presenta una nueva característica denominada arranque seguro, que protege la configuración de arranque de Windows y los componentes, y carga un controlador antimalware de inicio temprano (ELAM). Este controlador se inicia antes que otros controladores de arranque y habilita la evaluación de esos controladores y ayuda al kernel de Windows a decidir si deben inicializarse.

## <a name="manifestation"></a>Manifestación

Al iniciarse primero por el kernel, ELAM se asegura de que se inicie antes que cualquier software de terceros y, por lo tanto, puede detectar malware en el proceso de arranque e impedir que se inicialice.

## <a name="mitigation"></a>Mitigación

Los controladores de arranque se inicializan en función de la clasificación que se devuelve desde el controlador ELAM según una directiva de inicialización. De forma predeterminada, la Directiva inicializa controladores conocidos y desconocidos, pero no inicializará controladores no válidos conocidos. Un administrador del sistema puede especificar una directiva personalizada a través de directiva de grupo que puede impedir que los controladores desconocidos se inicialicen o puedan habilitar los controladores que son críticos para el proceso de arranque, pero que se han alterado, el arranque se ha modificado.

## <a name="solution"></a>Solución

Un controlador ELAM debe registrarse para que las devoluciones de llamada de kernel obtengan información acerca de cada controlador de inicio de arranque mientras se está inicializando. El controlador ELAM puede devolver una clasificación para cada controlador. Estas funciones son necesarias:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

También se puede registrar un controlador ELAM para las devoluciones de llamada del registro. Al hacerlo, se habilita el controlador ELAM para inspeccionar los datos de configuración que usa cada controlador de inicio de arranque. El controlador ELAM puede, a continuación, bloquear o modificar los datos antes de que los usen los controladores de inicio de arranque, si es necesario. Estas funciones son necesarias:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Para obtener más información sobre los requisitos del controlador de ELAM y el uso de la API, vea [antimalware de inicio temprano](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Pruebas

Los controladores de ELAM deben estar firmados especialmente por Microsoft para asegurarse de que los inicia el kernel de Windows en las primeras fases del proceso de arranque. Para obtener la firma, los controladores de ELAM deben pasar un conjunto de pruebas de certificación para comprobar el rendimiento y el comportamiento. Estas pruebas se incluyen en el kit de certificación de hardware de Windows.

## <a name="resources"></a>Recursos

-   [Antimalware de inicio temprano](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Certificación de hardware con el kit de certificación de hardware de Windows presentación de la Conferencia de compilación](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Descargar kits y herramientas](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
