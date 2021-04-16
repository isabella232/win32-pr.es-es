---
description: WMI tiene varios objetos auxiliares de scripting que proporcionan las conversiones requeridas por los scripts.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Objetos auxiliares de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715757"
---
# <a name="scripting-helper-objects"></a>Objetos auxiliares de scripting

WMI tiene varios objetos auxiliares de scripting que proporcionan las conversiones requeridas por los scripts.

Los objetos auxiliares de scripting de WMI incluyen:

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Los objetos auxiliares desglosan las estructuras de datos compuestas para que no sea necesario un script para analizar la estructura y obtener cualquiera de las partes. Por ejemplo, la estructura **DateTime de WMI** no se puede mostrar directamente y es diferente de otras estructuras de datos DateTime de Windows, como la **\_ fecha VT**.

## <a name="swbemdatetime"></a>SWbemDateTime

El objeto [**SWbemDateTime**](swbemdatetime.md) proporciona propiedades que analizan el día, el mes, el año, la hora del día, etc. También proporciona métodos de conversión para convertir el valor DateTime de Instrumental de administración de Windows (WMI) a y desde [**los formatos de**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) **\_ fecha** y hora de VT. Para la configuración de seguridad de Internet Explorer (IE), el objeto **SWbemDateTime** es el único objeto de scripting de WMI que está marcado como Safe para la inicialización y seguro para el scripting. Para obtener más información y ejemplos de conversiones de fecha y hora, vea [fechas y horas](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) , y el artículo en TechNet ScriptCenter [sobre el tiempo (Oh, y sobre las fechas)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="swbemobjectpath"></a>SWbemObjectPath

Las propiedades de [**SWbemObjectPath**](swbemobjectpath.md) proporcionan la ruta de acceso absoluta de un objeto, pero también dividen las partes de la ruta de acceso WMI, como servidor, espacio de nombres, clase o ruta de acceso relativa. El objeto le permite establecer la seguridad de la ruta de acceso, obtener los valores de clave de los objetos que representan la ruta de acceso, determinar si un objeto es un singleton, etc. Para obtener más información sobre cómo trabajar con rutas de acceso a objetos WMI, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>Win32 \_ SecurityDescriptorHelper

La [**clase \_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) convierte el descriptor de seguridad de un objeto protegible de un formato a otro.

Muchos objetos, como las impresoras, los espacios de nombres WMI, las claves del registro o las aplicaciones DCOM, tienen descriptores de seguridad que controlan el acceso al objeto. Puede usar WMI para detectar o cambiar quién tiene acceso a estos objetos mediante la obtención o configuración del descriptor de seguridad asociado al objeto.

Sin embargo, los distintos métodos pueden obtener descriptores de seguridad en una matriz de bytes binaria, un formato de [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) o como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). La forma de matriz de bytes binaria de un descriptor de seguridad no debe manipularse, excepto por los métodos de C++ diseñados para [las operaciones de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-operations). Los descriptores de SDDL están en cadenas, pero siguen siendo difíciles de manipular. El formato más sencillo para manipular es **Win32 \_ SecurityDescriptor**, porque contiene objetos incrustados para el administrador de confianza, ACE y SID. Para obtener más información sobre la estructura de descriptores de seguridad en WMI, vea [objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md). Para obtener más información sobre cómo realizar conversiones, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
