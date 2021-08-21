---
description: El proveedor Windows Driver Model (WDM) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Acceso a datos desde controladores de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131918"
---
# <a name="accessing-data-from-device-drivers"></a>Acceso a datos desde controladores de dispositivos

El proveedor Windows Driver Model (WDM) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM. Las clases de los controladores de hardware residen en el espacio \\ \\ de nombres wmi \\ raíz.

El proveedor de WDM es de interés para aquellos que escriben controladores de dispositivos y para los administradores que están interesados en los datos del controlador de dispositivo.

En este tema se de abordan las secciones siguientes:

-   [Información para escritores de controladores de dispositivos](#information-for-device-driver-writers)
-   [Información para administradores y usuarios de datos de controladores](#information-for-administrators-and-users-of-driver-data)
-   [Temas relacionados](#related-topics)

## <a name="information-for-device-driver-writers"></a>Información para escritores de controladores de dispositivos

Las clases WMI relacionadas con un controlador de dispositivo específico se crean cuando el proveedor de WDM extrae el MOF binario del archivo ejecutable del controlador de dispositivo. Esto tiene lugar siempre que se inicia WMI, se instala un nuevo controlador de dispositivo o se elimina la instancia de [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) para un controlador determinado. Al comprobar Wmiprov.log, puede determinar si se produjo un error al extraer el archivo MOF binario. Los detalles [de los errores de mofcomp](mofcomp.md) se notifican en Mofcomp.log. Para obtener más información, vea [Archivos de registro WMI.](wmi-log-files.md) Por motivos de rendimiento, el proveedor de WDM no genera eventos al crear o eliminar clases debido a un inicio o detención de un proveedor de WDM.

El proveedor WDM transforma todos los datos WNODE en información de clase. Si se produce un error al transformar los datos de WNODE en datos de clase, se notifica en Wmiprov.log con el encabezado con formato y bytes representados en el mismo formato que un volcado de memoria.

Los cambios realizados en la configuración de seguridad del controlador no tienen efecto hasta que el proveedor de WDM se descarga y se vuelve a cargar. Para obtener más información, [vea Descargar un proveedor](unloading-a-provider.md).

WMI también puede hacer que los contadores de alto rendimiento para los controladores de hardware estén disponibles. Para obtener más información sobre cómo crear clases de alto rendimiento y mostrar datos en el Monitor de sistema de Perfmon, vea [Improving the Efficiency of an Instance Provider](improving-the-efficiency-of-an-instance-provider.md). Para obtener más información sobre cómo escribir controladores de dispositivo habilitados para WMI, vea [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Para obtener más información sobre los calificadores específicos de WDM en el archivo MOF, vea [**Calificadores específicos del proveedor de WDM.**](qualifiers-specific-to-the-wdm-provider.md)

## <a name="information-for-administrators-and-users-of-driver-data"></a>Información para administradores y usuarios de datos de controladores

Enumerar las instancias de la [clase WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) proporciona una lista de los controladores del sistema e información sobre si el proveedor de WDM ha logrado compilar correctamente los MOF para cada controlador. Puede forzar al proveedor a volver a compilar y volver a generar las clases de un controlador mediante la eliminación de la instancia de WMIBinaryMofResource que representa ese controlador. Los detalles de los errores de [mofcomp](mofcomp.md) se notifican en Mofcomp.log.

Si el espacio de nombres WMI está dañado, se puede eliminar y volver a abrir para forzar a WDM a volver a generar las clases de controlador. Para obtener más información sobre cómo abrir un espacio de nombres, vea [Crear jerarquías dentro de WMI.](creating-hierarchies-within-wmi.md)

En ocasiones, las clases de controlador pueden "desenlazado" si se interrumpe la carga del controlador o se producen otras operaciones anómalas. El proveedor de WDM solo buscará y limpiará las clases "desenlazados" cuando se instale un nuevo controlador o cuando el valor de clave del Registro **ProcessClassedClasses** de **\\ Microsoft \\ WBEM \\** de Software esté establecido en **TRUE.** Establecer este valor en **TRUE ralentiza** el rendimiento de inicio de WMI debido a la operación de limpieza. El valor predeterminado es **FALSE**. El proveedor WDM solo comprueba este valor del Registro cuando el espacio de nombres \\ "Wmi raíz" se abre por primera vez.

Si se realizan cambios de seguridad en un controlador de dispositivo WDM, los cambios no se harán efectivos hasta que el proveedor de WDM se descargue y se vuelva a cargar. El Windows management debe detenerse y reiniciarse para lograr esto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de WMI](using-wmi.md)
</dt> </dl>

 

 
