---
description: Las clases de C++ de WMI que forman parte del marco de proveedores WMI ya no se recomiendan para su uso.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Clases de utilidad del marco de trabajo del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254a1321ab835c86e7b4bf0e5cb14048be0352290707a61aaf993a9a6cc6e8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130987"
---
# <a name="provider-framework-utility-classes"></a>Clases de utilidad del marco de trabajo del proveedor

\[Las clases de C++ de WMI que forman parte del marco de proveedores WMI que ahora se consideran en estado final, y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afectan a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el nuevo desarrollo.\]

Las bibliotecas del marco de Framedyd.dll (versión de depuración) y Framedyn.dll (versión de lanzamiento) implementan varias clases auxiliares de proveedor. Algunas funciones de Framedyn.dll se han quitado de los archivos de encabezado. Para seguir usando estas funciones, agregue `#define FRAMEWORK_ALLOW_DEPRECATED` al código antes de incluir Fwcommon.h.

Puede descargar proveedores individuales que ya no son necesarios.

Para usar esta funcionalidad, debe realizar los tres cambios siguientes en el proveedor en MainDll.cpp:

-   En la función **DllMain** donde se llama a [**CWbemProviderGlue::FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), debe agregar un segundo parámetro que sea un puntero a un largo.
-   En la función **DllCanUnloadNow** donde se llama a [**CWbemProviderGlue::FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), debe agregar un segundo parámetro que sea un puntero a un largo.
-   En la función **DllGetClassObject** donde se crea una instancia de **CWbemGlueFactory,** debe agregar un parámetro que sea un puntero a un valor long.

En los tres casos, el puntero a un objeto long debe ser el mismo puntero.

> [!Note]  
> En Maindll.cpp, las rutinas **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer,** **DllUnregisterServer** y **DllMain** deben encapsularse en un bloque try/catch.

 

> [!Caution]  
> Vínculo de compilaciones de depuración del proveedor con Framedyd.lib para Framedyd.dll. Framedyd.dll está en el directorio bin del Kit de desarrollo de software (SDK) de Microsoft Windows, que \\ no se incluye en la ruta de acceso del sistema. Cuando se prueba una compilación de depuración de un proveedor con el servicio de administración de Windows, el proveedor del marco no se cargará porque Framedyd.dll o una de sus dependencias no se encontrarán. Por lo tanto, debe copiar Framedyd.dll desde el directorio bin del SDK de Windows al directorio \\ \\ system32 wbem o agregar el directorio bin del SDK de Windows a la ruta de acceso de búsqueda del \\ \\ sistema.

 

En la tabla siguiente se enumeran las clases de utilidad del marco de trabajo del proveedor.



| Clase de utilidad                                          | Descripción                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Proporciona funciones de comparación y manipulación de cadenas para WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contiene para crear y manipular matrices de CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede acceso a una clase contenedora para los punteros.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilita las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contiene funciones auxiliares que se usan para calcular y mantener la diferencia de intervalo de tiempo entre dos [**objetos WBEMTime.**](wbemtime.md) |



 

> [!Note]  
> Las [**clases CHString**](chstring.md) y [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) son similares a las clases Microsoft Foundation Classes (MFC) **CString** y **CStringArray**. Las versiones de WMI existen para que los desarrolladores puedan acceder a métodos de comparación y manipulación de cadenas sin tener que tener acceso a MFC. Las [**clases WBEMTime**](wbemtime.md) y [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) también son similares a las clases **CTime** y **CTimeSpan de** MFC. Las versiones wmi son capaces de almacenar el tiempo hasta la precisión de nanosegundos y también pueden convertir a y desde **BSTR**. Para obtener más información sobre las clases CString, CStringArray, CTime y CTimeSpan, vea el [Microsoft Foundation Classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) en MSDN.

 

**Los valores BSTR** devueltos por [**los métodos WBEMTime**](wbemtime.md) están en formato de fecha y [hora:](date-and-time-format.md)"aaaammddHHMMSS.mmmmmmsUUU"

**Los valores BSTR** devueltos por [**los métodos WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) están en formato [de](interval-format.md)intervalo: "dddddddHHMMSS.mmmmmm:000"

Aunque las horas y los intervalos de tiempo se almacenan internamente como nanosegundos, no necesariamente se almacenan con precisión de nanosegundos. Esto se debe a que los objetos [**WBEMTime**](wbemtime.md) se pueden construir con formatos de tiempo que son precisos para un segundo (**struct tm** y **time \_ t**). Agregar posiciones decimales artificiales no aumenta la precisión.

 

 
