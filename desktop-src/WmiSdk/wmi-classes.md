---
description: En esta sección se proporciona información sobre la clase WMI y la página de referencia.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Clases WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706152"
---
# <a name="wmi-classes"></a>Clases WMI

En esta sección se proporciona información sobre la clase WMI y la página de referencia. Para obtener más información sobre cómo recuperar datos de clase o instancia, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md). En la lista siguiente se enumeran, describen y proporcionan vínculos a información específica de la clase WMI. Para obtener más información y ejemplos de código de script sobre el uso de clases de WMI para obtener una variedad de datos de hardware y de sistema operativo, vea [tareas de WMI para scripts y aplicaciones](wmi-tasks-for-scripts-and-applications.md). Para obtener ejemplos de C++, vea [ejemplos de aplicaciones de c++ en WMI](wmi-c---application-examples.md). La [conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) muestra cómo obtener datos remotos. También puede usar PowerShell para tener acceso a objetos WMI. para obtener una lista de las clases WMI que incluyen ejemplos de código de PowerShell, vea [aquí](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Sección                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Clases del sistema WMI](wmi-system-classes.md)               | Clases predefinidas que se incluyen en todos los espacios de nombres del núcleo Instrumental de administración de Windows (WMI). Puede reconocer una clase de sistema WMI porque el nombre comienza con un carácter de subrayado doble ( \_ \_ ). Estas clases proporcionan gran parte de la funcionalidad básica de WMI. Las clases del sistema WMI son similares en lo que respecta a las tablas del sistema de SQL Server. |
| [Clases MSFT](msft-classes.md)                           | Otras clases de Microsoft que ofrecen los medios para manipular varias características del sistema operativo, como eventos remotos y extensiones de directiva. Las clases de [solución de problemas de WMI](wmi-troubleshooting.md) son clases de msft que proporcionan datos sobre las operaciones de WMI.                                                                                               |
| [Clases CIM](cimclas.md)                                 | Clases de esquema de [*modelo de información común (CIM)*](gloss-c.md) . Si desea escribir sus propias clases WMI, puede heredar de una o varias de estas clases. Las [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider) de WMI heredan de las clases CIM.                                                                          |
| [Clases de consumidor estándar](standard-consumer-classes.md) | Un conjunto de consumidores de eventos de WMI que desencadenan una acción cuando se recibe un evento arbitrario. Para obtener más información, consulte [supervisión de eventos](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Ejemplos de código del centro de scripting de clase WMI

Los siguientes ejemplos de código del centro de scripting afectan a varias clases de WMI en varios espacios de nombres.



| Link                                                                                                                                      | Descripción                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Explorador WMI de GUI y generador de ayuda de métodos WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script de ejemplo que proporciona un explorador WMI de GUI y un generador de ayuda de método WMI.                                                                                                                                                        |
| [Explorador WMI buscar espacios de nombres WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Permite a los usuarios buscar clases en todos los espacios de nombres disponibles en los equipos especificados. Este ejemplo es el versión de línea de comandos del ejemplo del explorador WMI de la GUI y se puede considerar una extensión de Get-WmiObject-List. |
| [Herramienta de administración del sistema de Windows Arposh](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA se creó pensando en el administrador del sistema. La solución de problemas de Windows requiere una amplia gama de herramientas y conocimientos. AWSA pone esas herramientas juntas en una ubicación central y agrega funcionalidad adicional.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenciones de nomenclatura para las clases y propiedades de WMI

Los nombres de propiedad deben ajustarse a la sintaxis de Managed Object Format (MOF) definida por el equipo de administración distribuida (DTMF). Los caracteres de identificador inicial deben estar entre las letras de la a a la z y el carácter de subrayado ( \_ ). Todos los caracteres adicionales deben estar entre las letras de la a a la z, el carácter de subrayado y los números del 0 al 9. Para obtener más información, consulte la sección uso de Unicode de la [especificación CIM versión 2,2](https://www.dmtf.org/standards/cim).

Las palabras reservadas de SQL no se deben utilizar en los nombres de clase y propiedad. Para obtener una lista completa de las palabras reservadas de SQL y para obtener más información, vea la sección directrices de la [versión 2,2](https://www.dmtf.org/standards/cim)de la especificación de CIM.

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenciones de documentos para una página de referencia de clase WMI

En esta sección se identifican y describen las convenciones de documento de una página de referencia de clase WMI.

Una página de referencia típica contiene un bloque de sintaxis, una tabla de métodos y una lista de propiedades.

-   Bloque de sintaxis

    Una versión simplificada del código MOF que incluye el nombre de clase, la clase primaria (si existe) y las propiedades de clase, en orden alfabético, con tipos de datos.

-   Tabla de métodos

    Si una clase tiene métodos, los métodos se enumeran en la tabla inmediatamente después del bloque de sintaxis. Cada método implementado se vincula a una página de referencia.

-   Lista Propiedades

    Cada propiedad de clase se muestra con un tipo de datos, un tipo de acceso (de solo lectura o de lectura/escritura), calificadores y una descripción de la propiedad.

## <a name="syntax-block"></a>Bloque de sintaxis

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabla de métodos



| \_Métodos XYZ de Win32 | Descripción                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Breve descripción de lo que hace el método. |



 

## <a name="properties-list"></a>Lista Propiedades

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>rotación
</dt> <dd>

Tipo de datos: **UInt16**

Tipo de acceso: muestra si tiene acceso de lectura/escritura o de solo lectura a esta propiedad.

Calificadores: Si está presente, muestra los calificadores de la propiedad. Por ejemplo, **clave**, **invalidación**.

Describe la propiedad y proporciona información de herencia para la propiedad. Por ejemplo, esta propiedad se hereda de **CIM \_* XYZ * * *. Hay un vínculo a la clase primaria si Microsoft proporciona una implementación de esa clase. Sin embargo, las clases CIM no están disponibles.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Descripción de la propiedad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Proporciona más información sobre la clase, si procede. También proporciona información de derivación, si procede.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
