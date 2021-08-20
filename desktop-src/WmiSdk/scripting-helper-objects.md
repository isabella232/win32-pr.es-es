---
description: WMI tiene varios objetos auxiliares de scripting que suministran las conversiones requeridas por los scripts.
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
ms.openlocfilehash: f205792bf76738e80b8dd703d40af894f7178fc8e59d92b60969c2a8f0670588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923061"
---
# <a name="scripting-helper-objects"></a>Objetos auxiliares de scripting

WMI tiene varios objetos auxiliares de scripting que suministran las conversiones requeridas por los scripts.

Los objetos auxiliares de scripting wmi incluyen:

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**Seguridad de \_ Win32DescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Los objetos auxiliares descomponen las estructuras de datos compuestos para que no sea necesario un script para analizar la estructura y obtener cualquiera de las piezas. Por ejemplo, la **estructura DATETIME de WMI** no se puede mostrar directamente y es diferente de otras estructuras de datos Windows fecha y hora, como VT **\_ DATE**.

## <a name="swbemdatetime"></a>SWbemDateTime

El [**objeto SWbemDateTime**](swbemdatetime.md) proporciona propiedades que analizan el día, el mes, el año, la hora del día, y así sucesivamente. También proporciona métodos de conversión para convertir la fecha y hora de Windows Management Instrumentation (WMI) a y desde los formatos **VT \_ Date** [**y FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) Para Internet Explorer de seguridad (IE), el objeto **SWbemDateTime** es el único objeto de scripting WMI que se marca como seguro para inicialización y seguro para scripting. Para obtener más información y ejemplos de [](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) conversiones de fecha y hora, vea Fechas y horas y el artículo sobre TechNet ScriptCenter [It's About Time (Oh, and About Dates, too) (TechNet ScriptCenter It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx)[Acerca de las fechas y las fechas de TechNet]).

## <a name="swbemobjectpath"></a>SWbemObjectPath

Las propiedades de [**SWbemObjectPath**](swbemobjectpath.md) suministran la ruta de acceso absoluta de un objeto, pero también separan las partes de la ruta de acceso WMI, como el servidor, el espacio de nombres, la clase o la ruta de acceso relativa. El objeto permite establecer la seguridad de la ruta de acceso, obtener los valores de clave de los objetos que representan la ruta de acceso, determinar si un objeto es un singleton, y así sucesivamente. Para obtener más información sobre cómo trabajar con rutas de acceso de objetos WMI, vea [Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>Seguridad de \_ Win32DescriptorHelper

La [**clase \_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) convierte el descriptor de seguridad de un objeto protegible de un formato a otro.

Muchos objetos, como impresoras, espacios de nombres WMI, claves del Registro o aplicaciones DCOM, tienen descriptores de seguridad que controlan el acceso al objeto. Puede usar WMI para detectar o cambiar quién tiene acceso a estos objetos obteniendo o estableciendo el descriptor de seguridad asociado al objeto.

Sin embargo, distintos métodos pueden obtener descriptores de seguridad en una matriz de bytes [binaria,](/windows/desktop/SecAuthZ/security-descriptor-string-format) en formato de lenguaje de definición de descriptores de seguridad (SDDL) o como una instancia de [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) La forma de matriz de bytes binario de un descriptor de seguridad no debe manipularse excepto mediante los métodos de C++ diseñados para operaciones [de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-operations). Los descriptores de SDDL están en cadenas, pero siguen siendo difíciles de manipular. El formato más fácil de manipular **es \_ SecurityDescriptor de Win32,** ya que contiene objetos incrustados para administrador de confianza, ACE y SID. Para obtener más información sobre la estructura de descriptores de seguridad en WMI, vea [Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md). Para obtener más información sobre cómo realizar conversiones, vea Cambiar la seguridad [de acceso en objetos protegibles.](changing-access-security-on-securable-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
