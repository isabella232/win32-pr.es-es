---
description: Describe las convenciones de documento para leer temas de WMI Scripting API.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Convenciones de documento para Scripting API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575352"
---
# <a name="document-conventions-for-the-scripting-api"></a>Convenciones de documento para Scripting API

La [referencia de Scripting API para WMI](scripting-api-for-wmi.md) usa las siguientes convenciones de documento:

-   Los tipos de parámetro se definen mediante un prefijo: b (booleano), str (cadena), I (entero), obj (objeto de Automation), var (Variant).
-   Los parámetros opcionales se colocan entre corchetes con sus valores predeterminados mostrados por asignación.
-   En el caso de los parámetros de objeto, los caracteres situados después del prefijo "obj" indican el tipo de objeto esperado.



| Parámetro de objeto      | Tipo de objeto                                          |
|-----------------------|------------------------------------------------------|
| *WbemDatetime*        | [**SWbemDateTime**](swbemdatetime.md)               |
| *WbemEventSource*     | [**SWbemEventSource**](swbemeventsource.md)         |
| *WbemLocator*         | [**SWbemLocator**](swbemlocator.md)                 |
| *WbemMethod*          | [**SWbemMethod**](swbemmethod.md)                   |
| *WbemMethodSet*       | [**SWbemMethodSet**](swbemmethodset.md)             |
| *WbemNamedValueSet*   | [**SWbemNamedValueSet**](swbemnamedvalueset.md)     |
| *WbemObject*          | [**SWbemObject**](swbemobject.md)                   |
| *WbemObjectEx*        | [**SWbemObjectEx**](swbemobjectex.md)               |
| *WbemObjectPath*      | [**SWbemObjectPath**](swbemobjectpath.md)           |
| *WbemObjectSet*       | [**SWbemObjectSet**](swbemobjectset.md)             |
| *WbemPrivilege*       | [**SWbemPrivilege**](swbemprivilege.md)             |
| *WbemPrivilegeSet*    | [**SWbemPrivilegeSet**](swbemprivilegeset.md)       |
| *WbemProperty*        | [**SWbemProperty**](swbemproperty.md)               |
| *WbemPropertySet*     | [**SWbemPropertySet**](swbempropertyset.md)         |
| *WbemQualifier*       | [**SWbemQualifier**](swbemqualifier.md)             |
| *WbemQualifierSet*    | [**SWbemQualifierSet**](swbemqualifierset.md)       |
| *WbemRefreshableItem* | [**SWbemRefreshableItem**](swbemrefreshableitem.md) |
| *WbemRefresher*       | [**SWbemRefresher**](swbemrefresher.md)             |
| *WbemServices*        | [**SWbemServices**](swbemservices.md)               |
| *WbemServicesEx*      | [**SWbemServicesEx**](swbemservicesex.md)           |



 

Por ejemplo, el código siguiente muestra cómo dar nombre a variables para distintos tipos de objetos:


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



