---
title: Antimalware de inicio temprano
description: Antimalware de inicio temprano
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1ca8e52f9d2465038e68b6b585bed70b974432566b3b67d080c97bb998103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852201"
---
# <a name="early-launch-antimalware"></a>Antimalware de inicio temprano

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  

## <a name="description"></a>Descripción

A medida que el software antimalware (AM) se ha vuelto mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también están mejorando en la creación de rootkits que pueden ocultarse de la detección. Detectar malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM abordan diligentemente. Normalmente, crean ataques informáticos del sistema que no son compatibles con el sistema operativo host y pueden dar lugar a la colocación del equipo en un estado inestable. Hasta este momento, Windows ha proporcionado una buena manera de que AM detecte y resuelva estas amenazas de arranque temprano.

Windows 8 presenta una nueva característica denominada Arranque seguro, que protege la configuración y los componentes de arranque de Windows, y carga un controlador antimalware de inicio temprano (ELAM). Este controlador se inicia antes que otros controladores de arranque, habilita la evaluación de esos controladores y ayuda al kernel Windows a decidir si se deben inicializar.

## <a name="manifestation"></a>Manifestación

Al iniciarse primero mediante el kernel, se garantiza que ELAM se inicia antes que cualquier software de terceros y, por tanto, es capaz de detectar malware en el proceso de arranque e impedir que se inicializa.

## <a name="mitigation"></a>Mitigación

Los controladores de arranque se inicializan en función de la clasificación que se devuelve desde el controlador ELAM según una directiva de inicialización. De forma predeterminada, la directiva inicializa controladores conocidos buenos y desconocidos, pero no inicializará controladores no conocidos. Un administrador del sistema puede especificar una directiva personalizada a través de directiva de grupo que pueda impedir la inicialización de controladores desconocidos o puede permitir que se inicialicen los controladores que son críticos para el proceso de arranque, pero que se han alterado, arranque.

## <a name="solution"></a>Solución

Un controlador ELAM debe registrarse para las devoluciones de llamada del kernel para obtener información sobre cada controlador de inicio de arranque a medida que se está inicializando. A continuación, el controlador ELAM puede devolver una clasificación para cada controlador. Estas funciones son necesarias:

-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

Un controlador ELAM también puede registrarse para las devoluciones de llamada del Registro. Esto permite al controlador ELAM inspeccionar los datos de configuración que usa cada controlador de inicio de arranque. A continuación, el controlador ELAM puede bloquear o modificar los datos antes de que los utilicen los controladores de arranque, si es necesario. Estas funciones son necesarias:

-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

Para obtener más información sobre los requisitos del controlador ELAM y el uso de API, vea [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).

## <a name="tests"></a>Pruebas

Los controladores DE ELAM deben estar firmados especialmente por Microsoft para asegurarse de que el kernel Windows al principio del proceso de arranque. Para obtener la firma, los controladores de ELAM deben pasar un conjunto de pruebas de certificación para comprobar el rendimiento y otro comportamiento. Estas pruebas se incluyen en el kit Windows de certificación de hardware.

## <a name="resources"></a>Recursos

-   [Antimalware de inicio temprano](/windows-hardware/drivers/install/early-launch-antimalware)
-   [CmRegisterCallbackEx](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [CmUnRegisterCallback](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [IoRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [IoUnRegisterBootDriverCallback](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [Certificación de hardware con la presentación de la conferencia de compilación Windows Kit de certificación de hardware](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [Descargar kits y herramientas](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
