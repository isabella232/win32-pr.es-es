---
description: En esta sección se proporciona información sobre la clase WMI y la página de referencia.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Clases WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359207"
---
# <a name="wmi-classes"></a>Clases WMI

En esta sección se proporciona información sobre la clase WMI y la página de referencia. Para obtener más información sobre cómo recuperar datos de clase o instancia, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md). En la lista siguiente se enumeran, describen y proporcionan vínculos a información de clase WMI específica. Para obtener más información y ejemplos de código de script del uso de clases WMI para obtener una variedad de datos de hardware y sistema operativo, vea Tareas WMI para [scripts y aplicaciones.](wmi-tasks-for-scripts-and-applications.md) Para obtener ejemplos en C++, vea [Wmi C++ Application Examples](wmi-c---application-examples.md). [Conectarse a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) muestra cómo obtener datos remotos. También puede usar PowerShell para acceder a objetos WMI; Para obtener una lista de clases WMI que incluyen ejemplos de código de PowerShell, [consulte aquí](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Sección                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Clases del sistema WMI](wmi-system-classes.md)               | Clases predefinidas que se incluyen en todos los espacios de nombres del Windows de Instrumental de administración de recursos (WMI). Puede reconocer una clase del sistema WMI porque el nombre comienza con un carácter de subrayado doble ( \_ \_ ). Estas clases proporcionan gran parte de la funcionalidad básica para WMI. Las clases del sistema WMI son similares a las tablas del sistema en SQL servidor. |
| [Clases MSFT](msft-classes.md)                           | Otras clases de Microsoft que ofrecen los medios para manipular varias características del sistema operativo, como eventos remotos y extensiones de directiva. Las [clases de solución de problemas de WMI](wmi-troubleshooting.md) son clases MSFT que proporcionan datos sobre las operaciones WMI.                                                                                               |
| [Clases CIM](cimclas.md)                                 | [*Modelo de información común de esquema (CIM).*](gloss-c.md) Si desea escribir sus propias clases WMI, puede heredar de una o varias de estas clases. Las clases [Win32 de](/windows/desktop/CIMWin32Prov/win32-provider) WMI heredan de las clases CIM.                                                                          |
| [Clases de consumidor estándar](standard-consumer-classes.md) | Conjunto de consumidores de eventos WMI que desencadenan una acción tras la recepción de un evento arbitrario. Para obtener más información, vea [Monitoring Events](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Ejemplos de código del Centro de scripting de clases WMI

Los siguientes ejemplos de código del Centro de scripting afectan a varias clases WMI en varios espacios de nombres.



| Vínculo                                                                                                                                      | Descripción                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Explorador WMI de GUI y generador de ayuda de métodos WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Script de ejemplo que proporciona un Explorador WMI de GUI y un Generador de ayuda de métodos WMI.                                                                                                                                                        |
| [Espacios de nombres WMI de búsqueda del Explorador WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Permite a los usuarios buscar clases en todos los espacios de nombres disponibles en los equipos especificados. Este ejemplo es la verison de línea de comandos del ejemplo del Explorador WMI de GUI y se puede considerar una extensión de Get-WmiObject -List. |
| [Arposh Windows de administración del sistema](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA se creó pensando en el administrador del sistema. La solución Windows problemas requiere una amplia gama de herramientas y conocimientos. AWSA reúne esas herramientas en una ubicación central y agrega funcionalidad adicional.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Convenciones de nomenclatura para clases y propiedades WMI

Los nombres de propiedad deben cumplir la sintaxis Managed Object Format (MOF) definida por el Grupo de tareas de administración distribuida (DTMF). Los caracteres de identificador inicial deben ser de las letras a a a z y el carácter de subrayado ( \_ ). Todos los caracteres adicionales deben ser de las letras a a z, el carácter de subrayado y los números del 0 al 9. Para obtener más información, vea la sección Uso de Unicode de la [especificación CIM versión 2.2.](https://www.dmtf.org/standards/cim)

SQL las palabras de reserva no se deben usar en los nombres de clase y propiedad. Para obtener una lista completa de los SQL reservar palabras y para obtener más información, vea la sección Directrices de la especificación [CIM versión 2.2.](https://www.dmtf.org/standards/cim)

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Convenciones de documento para una página de referencia de clase WMI

En esta sección se identifican y describen las convenciones de documento para una página de referencia de clase WMI.

Una página de referencia típica contiene un bloque de sintaxis, una tabla de métodos y una lista de propiedades.

-   Bloque de sintaxis

    Una versión simplificada del código MOF que incluye el nombre de clase, la clase primaria (si la hay) y las propiedades de clase, en orden alfabético, con tipos de datos.

-   Tabla de métodos

    Si una clase tiene métodos, los métodos se muestran en la tabla inmediatamente después del bloque de sintaxis. Cada método implementado está vinculado a una página de referencia.

-   Lista Propiedades

    Cada propiedad de clase se muestra con un tipo de datos, un tipo de acceso (de solo lectura o lectura/escritura), calificadores y una descripción de la propiedad.

## <a name="syntax-block"></a>Bloque de sintaxis

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Tabla de métodos



| Métodos xyz de Win32 \_ | Descripción                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Breve descripción de lo que hace el método. |



 

## <a name="properties-list"></a>Lista Propiedades

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>Abc
</dt> <dd>

Tipo de datos: **uint16**

Tipo de acceso: muestra si tiene acceso de lectura/escritura o de solo lectura a esta propiedad.

Calificadores: si está presente, muestra los calificadores de la propiedad . Por ejemplo, **Key**, **Override**.

Describe la propiedad y proporciona información de herencia para la propiedad . Por ejemplo, esta propiedad se hereda de **CIM \_* xyz).. Hay un vínculo a la clase primaria si Microsoft proporciona una implementación de esa clase. Sin embargo, las clases CIM no están disponibles.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>Def
</dt> <dd>

Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Descripción de la propiedad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Proporciona más información sobre la clase , si procede. También proporciona información de derivación, si procede.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> </dl>

 

 
