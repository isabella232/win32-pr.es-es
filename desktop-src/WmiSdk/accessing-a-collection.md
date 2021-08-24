---
description: Una colección es un concepto de automatización estándar que proporciona una interfaz uniforme a un conjunto de objetos sobre los que se puede realizar la iteración.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Acceso a una colección WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860521"
---
# <a name="accessing-a-wmi-collection"></a>Acceso a una colección WMI

Una colección es un concepto de automatización estándar que proporciona una interfaz uniforme a un conjunto de objetos sobre los que se puede realizar la iteración. Scripting API para WMI expone una serie de interfaces que se ajustan al paradigma de colección. En cada caso, use el **método Item** para identificar los elementos mediante una cadena que contiene el valor.

Las [**colecciones SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)y [**SWbemMethodSet**](swbemmethodset.md) se usan principalmente para modificar el esquema. Un [**objeto SWbemObjectSet**](swbemobjectset.md) contiene objetos WMI, como una instancia de [**\_ LogicalDisk de Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que se han obtenido a través de llamadas, como [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) o [**SWbemObject.Associators. \_**](swbemobject-associators-.md) El [**objeto SWbemRefresher**](swbemrefresher.md) solo puede contener instancias de clases WMI. El [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) puede contener objetos WMI o cualquier otro tipo de datos que un proveedor requiera para la llamada al método.

> [!Note]  
> Los temas siguientes se escribieron principalmente para VBScript. C# usa la interfaz [IEnumerable](/dotnet/api/system.collections.ienumerable) estándar para intercalar y enumerar objetos. Por el contrario, PowerShell suele usar una colección implícita de objetos siempre que un valor devuelto contenga más de un resultado.

 

En la tabla siguiente se enumeran las colecciones de Scripting API para WMI y los elementos y parámetros de cada colección.



| Colección                                       | Elemento                                              | Item() (Parámetro)                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Ruta de acceso al objeto                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Nombre de propiedad                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Nombre del calificador                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nombre del método                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nombre del valor                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nombre de privilegio                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Índice del elemento en el [**objeto SWbemRefresher**](swbemrefresher.md) |



 

Para obtener más información y ejemplos de cómo agregar [](removing-a-single-item-from-a-collection.md) y quitar elementos de una colección, vea Quitar un único elemento de una colección y Quitar varios elementos [de una colección](removing-multiple-items-from-a-collection.md). Para obtener más información sobre cómo trabajar con clases, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).

 

 
