---
description: El proveedor de Modelo de controlador de Windows (WDM) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Acceder a los datos desde los controladores de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a59b59116ca0f71178fb2faed290d6bc76c9d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707411"
---
# <a name="accessing-data-from-device-drivers"></a>Acceder a los datos desde los controladores de dispositivos

El proveedor de Modelo de controlador de Windows (WDM) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM. Las clases para los controladores de hardware residen en el \\ \\ \\ espacio de nombres WMI raíz.

El proveedor de WDM es de interés para los usuarios que escriben controladores de dispositivos y para los administradores interesados en los datos de controladores de dispositivos.

En este tema se describen las siguientes secciones:

-   [Información para escritores de controladores de dispositivos](#information-for-device-driver-writers)
-   [Información para administradores y usuarios de datos de controladores](#information-for-administrators-and-users-of-driver-data)
-   [Temas relacionados](#related-topics)

## <a name="information-for-device-driver-writers"></a>Información para escritores de controladores de dispositivos

Las clases WMI relacionadas con un controlador de dispositivo específico se crean cuando el proveedor de WDM extrae el MOF binario del archivo ejecutable del controlador de dispositivo. Esto tiene lugar cuando se inicia WMI, se instala un nuevo controlador de dispositivo o se elimina la instancia de [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) para un controlador determinado. Al comprobar Wmiprov. log, puede determinar si se produjo un error al extraer el archivo MOF binario. Los detalles de los errores de [MOFCOMP](mofcomp.md) se muestran en MOFCOMP. log. Para obtener más información, consulte [archivos de registro de WMI](wmi-log-files.md). Por motivos de rendimiento, el proveedor de WDM no genera eventos al crear o eliminar clases debido a que un proveedor de WDM se inicia o se detiene.

El proveedor de WDM transforma todos los datos de WNODE en información de clase. Si se produce un error al transformar los datos de WNODE en datos de clase, se notifica en Wmiprov. log con el encabezado con formato y los bytes representados en el mismo formato que un volcado de memoria.

Los cambios realizados en la configuración de seguridad del controlador no surtirán efecto hasta que el proveedor de WDM se descargue y se vuelva a cargar. Para obtener más información, vea [descargar un proveedor](unloading-a-provider.md).

WMI también puede crear contadores de alto rendimiento para los controladores de hardware disponibles. Para obtener más información acerca de cómo crear clases de alto rendimiento y Mostrar datos en el monitor de sistema de Perfmon, consulte [mejorar la eficacia de un proveedor de instancias](improving-the-efficiency-of-an-instance-provider.md). Para obtener más información acerca de la escritura de controladores de dispositivos habilitados para WMI, consulte [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Para obtener más información acerca de los calificadores específicos de WDM en el archivo MOF, consulte [**calificadores específicos del proveedor de WDM**](qualifiers-specific-to-the-wdm-provider.md).

## <a name="information-for-administrators-and-users-of-driver-data"></a>Información para administradores y usuarios de datos de controladores

Al enumerar las instancias de la clase [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) , se proporciona una lista de los controladores del sistema e información sobre si el proveedor de WDM ha realizado correctamente la compilación de MOF para cada controlador. Puede forzar que el proveedor vuelva a compilar y regenerar las clases para un controlador eliminando la instancia de WMIBinaryMofResource que representa ese controlador. Los detalles de los errores de [MOFCOMP](mofcomp.md) se muestran en el archivo MOFCOMP. log.

Si el espacio de nombres WMI está dañado, se puede eliminar y volver a abrir para forzar a WDM a volver a generar las clases de controlador. Para obtener más información sobre cómo abrir un espacio de nombres, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).

En ocasiones, las clases de controlador pueden aparecer "en desuso" si se interrumpe la carga de controladores o se producen otras operaciones anómalas. El proveedor de WDM solo buscará y limpiará las clases "en desuso" cuando se instale un nuevo controlador o cuando el valor de clave del registro de **\\ Microsoft \\ WBEM \\ WDMProvider del software** **ProcessStrandedClasses** esté establecido en **true**. Si se establece este valor en **true** , se ralentiza el rendimiento de inicio de WMI debido a la operación de limpieza. El valor predeterminado es **FALSE**. El proveedor de WDM solo comprueba este valor del registro cuando \\ se abre por primera vez el espacio de nombres "root WMI".

Si se realizan cambios de seguridad en un controlador de dispositivo WDM, los cambios no entrarán en vigor hasta que el proveedor de WDM se descargue y se vuelva a cargar. El servicio de administración de Windows debe detenerse y reiniciarse para lograrlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar WMI](using-wmi.md)
</dt> </dl>

 

 
