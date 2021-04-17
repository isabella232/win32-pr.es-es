---
description: Las clases de C++ de WMI que forman parte del marco de trabajo del proveedor de WMI ya no se recomiendan para su uso.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Clases de utilidad de Framework de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707283"
---
# <a name="provider-framework-utility-classes"></a>Clases de utilidad de Framework de proveedor

\[Las clases de C++ de WMI que forman parte del marco de trabajo del proveedor de WMI que ahora se consideran en estado final y no estarán disponibles más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Las bibliotecas del marco de trabajo del proveedor Framedyd.dll (versión de depuración) y Framedyn.dll (versión de lanzamiento) implementan varias clases auxiliares de proveedor. Algunas funciones de Framedyn.dll se han quitado de los archivos de encabezado. Para seguir usando estas funciones, agregue `#define FRAMEWORK_ALLOW_DEPRECATED` al código antes de incluir Fwcommon. h.

Puede descargar proveedores individuales que ya no son necesarios.

Para usar esta funcionalidad, debe realizar los tres cambios siguientes en el proveedor en MainDll. cpp:

-   En la función **DllMain** en la que se llama a [**CWbemProviderGlue:: FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), se debe agregar un segundo parámetro que sea un puntero a un Long.
-   En la función **DllCanUnloadNow** donde se llama a [**CWbemProviderGlue:: FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), debe agregar un segundo parámetro que sea un puntero a un Long.
-   En la función **DllGetClassObject** donde cree una instancia de **CWbemGlueFactory**, debe agregar un parámetro que sea un puntero a un Long.

En los tres casos, el puntero a un Long debe ser el mismo puntero.

> [!Note]  
> En las rutinas Maindll. cpp, **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** y **DllMain** se deben encapsular en un bloque try/catch.

 

> [!Caution]  
> Las compilaciones de depuración del proveedor vinculan con Framedyd. lib para Framedyd.dll. Framedyd.dll está en el directorio bin del kit de desarrollo de software (SDK) de Microsoft Windows, \\ que no se incluye en la ruta de acceso del sistema. Cuando se prueba una compilación de depuración de un proveedor con el servicio de administración de Windows, el proveedor de .NET Framework no se cargará porque no se encontrará Framedyd.dll o una de sus dependencias. Por lo tanto, debe copiar Framedyd.dll del directorio Windows SDK \\ bin en el \\ directorio system32 \\ WBEM o agregar el directorio Windows SDK \\ bin a la ruta de acceso de búsqueda del sistema.

 

En la tabla siguiente se enumeran las clases de la utilidad del marco del proveedor.



| Clase de utilidad                                          | Descripción                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Proporciona funciones de comparación y manipulación de cadenas para WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contiene para crear y manipular matrices de CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede acceso a una clase contenedora para los punteros.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilita las conversiones entre varios formatos de tiempo de ejecución de Windows y ANSI C.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contiene funciones auxiliares que se usan para calcular y mantener la diferencia de intervalo de tiempo entre dos objetos [**WBEMTime**](wbemtime.md) . |



 

> [!Note]  
> Las clases [**CHString**](chstring.md) y [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) son similares a las Microsoft Foundation Classes (MFC) **CString** y **CStringArray**. Las versiones de WMI existen para que los programadores puedan tener acceso a los métodos de manipulación y comparación de cadenas sin tener que tener acceso a MFC. Las clases [**WBEMTime**](wbemtime.md) y [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) también son similares a las clases **ctime** y **CTimeSpan** de MFC. Las versiones de WMI son capaces de almacenar el tiempo en la precisión de nanosegundos y también se pueden convertir en **BSTR** y desde este. Para obtener más información acerca de las clases CString, CStringArray, CTime y CTimeSpan, vea el [Microsoft Foundation Classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) en MSDN.

 

Los valores **BSTR** devueltos por los métodos [**WBEMTime**](wbemtime.md) están en [formato de fecha y hora](date-and-time-format.md): "aaaammddhhmmss. mmmmmmsUUU"

Los valores **BSTR** devueltos por los métodos [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) están en [formato de intervalo](interval-format.md): "ddddddddHHMMSS. mmmmmm: 000"

Aunque las horas y los intervalos de tiempo se almacenan internamente como nanosegundos, no se almacenan necesariamente con una precisión de nanosegundos. Esto se debe a que los objetos [**WBEMTime**](wbemtime.md) se pueden construir con formatos de hora con una precisión de un segundo (**struct TM** y **Time \_ t**). La adición de posiciones decimales artificiales no aumenta la precisión.

 

 
