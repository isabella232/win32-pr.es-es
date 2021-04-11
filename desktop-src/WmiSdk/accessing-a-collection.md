---
description: Una colección es un concepto de automatización estándar que proporciona una interfaz uniforme a un conjunto de objetos sobre el que se puede realizar la iteración.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Obtener acceso a una colección WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b875f50c1778a03c304f90c019da172be6ef5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278776"
---
# <a name="accessing-a-wmi-collection"></a>Obtener acceso a una colección WMI

Una colección es un concepto de automatización estándar que proporciona una interfaz uniforme a un conjunto de objetos sobre el que se puede realizar la iteración. La API de scripting para WMI expone una serie de interfaces que se ajustan al paradigma de la colección. En cada caso, use el método **Item** para identificar los elementos usando una cadena que contiene el valor.

Las colecciones [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)y [**SWbemMethodSet**](swbemmethodset.md) se usan principalmente para modificar el esquema. Un objeto [**SWbemObjectSet**](swbemobjectset.md) contiene objetos WMI, como una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , que se han obtenido a través de llamadas, como [**SWbemServices.**](swbemservices-instancesof.md) instanceof o [**SWbemObject. ASSOCIATORS \_**](swbemobject-associators-.md). El objeto [**SWbemRefresher**](swbemrefresher.md) solo puede contener instancias de clases WMI. El objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) puede contener objetos WMI o cualquier otro tipo de datos que un proveedor requiera para la llamada al método.

> [!Note]  
> Los temas siguientes se escribieron principalmente para VBScript. C# usa la interfaz [IEnumerable](/dotnet/api/system.collections.ienumerable) estándar para intercalar y enumerar objetos. En cambio, PowerShell suele usar una colección de objetos implícita siempre que un valor devuelto contiene más de un resultado.

 

En la tabla siguiente se enumeran las colecciones de la API de scripting para WMI y los elementos y parámetros de cada colección.



| Colección                                       | Elemento                                              | Parámetro Item ()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Ruta de objeto                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Nombre de propiedad                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Nombre del calificador                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nombre del método                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nombre del valor                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nombre del privilegio                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Índice del elemento en el objeto [**SWbemRefresher**](swbemrefresher.md) |



 

Para obtener más información sobre y ejemplos de cómo agregar y quitar elementos de una colección, vea [quitar un solo elemento de una colección](removing-a-single-item-from-a-collection.md) y [quitar varios elementos de una colección](removing-multiple-items-from-a-collection.md). Para obtener más información sobre cómo trabajar con clases, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md).

 

 
