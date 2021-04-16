---
description: Puede usar los métodos y las propiedades del objeto SWbemObject para representar una definición de clase Instrumental de administración de Windows (WMI) o una instancia de objeto.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Objeto SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706049"
---
# <a name="swbemobject-object"></a>Objeto SWbemObject

Puede usar los métodos y las propiedades del objeto **SWbemObject** para representar una definición de clase instrumental de administración de Windows (WMI) o una instancia de objeto. Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.

Este objeto admite dos tipos de propiedades y métodos. Los definidos en esta sección son propiedades y métodos genéricos que se aplican a todos los objetos de WMI. Además, este objeto expone las propiedades y los métodos del objeto subyacente como propiedades y métodos de automatización dinámica de **SWbemObject**. Los nombres y tipos de estas propiedades y métodos dependen del objeto WMI subyacente. Para obtener más información sobre cómo se exponen estas propiedades y métodos dinámicos, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md).

Desde la perspectiva del cliente WMI, este objeto siempre está en proceso. Las operaciones de escritura solo afectan a la copia local del objeto y las operaciones de lectura siempre recuperan los valores de la copia local. Las actualizaciones de WMI solo se realizan cuando se escriben objetos completos mediante una llamada al método [**SWbemObject \_ . put**](swbemobject-put-.md) . Si modifica las propiedades o los métodos en un objeto **SWbemObject** , los cambios no se escriben en WMI hasta que llame a **SWbemObject \_ . put**.

Los nombres de método y propiedad genéricos definidos en esta sección terminan siempre con un carácter de subrayado final (" \_ ") para diferenciarlos de los métodos y propiedades de WMI dinámicos del objeto subyacente.

Tenga en cuenta que **SWbemObject** no se puede crear con el método [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). de VBScript. Si desea crear una nueva clase vacía, use [**SWbemServices. Get**](swbemservices-get.md) con un parámetro de ruta de acceso vacío. Esta llamada devuelve un objeto **SWbemObject** vacío que puede convertirse en una clase. Después, puede proporcionar un nombre de clase para la propiedad de [**clase**](swbemobjectpath-class.md) del objeto [**SWbemObjectPath**](swbemobjectpath.md) devuelto por la llamada de [**ruta de acceso \_**](swbemobject-path-.md) . Agregue propiedades a la nueva clase mediante el [**método \_ Properties**](swbemobject-properties-.md) . Para crear una instancia, llame a **GetObject** en la nueva clase.

En el ejemplo de código siguiente se muestra cómo obtener una nueva clase y agregarle una propiedad. El objeto **SWbemObject** que representa la clase debe volver a escribirse en el repositorio WMI mediante una llamada [**a \_ Put**](swbemobject-put-.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



Puede examinar el repositorio con una herramienta de visualización como [CIM Studio](further-information.md) para comprobar que aparece la nueva clase e instancia. Para obtener un ejemplo de cómo quitar una clase y una instancia del repositorio, vea [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).

## <a name="members"></a>Miembros

El objeto **SWbemObject** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemObject** tiene estos métodos.



| Método                                                        | Descripción                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Asociadores\_**](swbemobject-associators-.md)             | Recupera los asociadores del objeto.<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | Recupera asincrónicamente los asociados del objeto.<br/>                                      |
| [**Clonar\_**](swbemobject-clone-.md)                         | Realiza una copia del objeto actual.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Comprueba la igualdad de dos objetos.<br/>                                                              |
| [**Elimínelos\_**](swbemobject-delete-.md)                       | Elimina el objeto de WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Elimina de forma asincrónica el objeto de WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Ejecuta un método exportado por un proveedor de métodos.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Ejecuta de forma asincrónica un método exportado por un proveedor de métodos.<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | Recupera la representación textual del objeto (sintaxis MOF).<br/>                             |
| [**Instancias\_**](swbemobject-instances-.md)                 | Devuelve una colección de instancias del objeto (que debe ser una clase WMI).<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | Devuelve de forma asincrónica una colección de instancias del objeto (que debe ser una clase WMI).<br/>  |
| [**Pondrán\_**](swbemobject-put-.md)                             | Crea o actualiza el objeto en WMI.<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | Crea o actualiza de forma asincrónica el objeto en WMI.<br/>                                         |
| [**Referencias\_**](swbemobject-references-.md)               | Devuelve las referencias al objeto.<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | Devuelve de forma asincrónica las referencias al objeto.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Crea una nueva clase derivada a partir del objeto actual (que debe ser una clase WMI).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Crea una nueva instancia de a partir del objeto actual.<br/>                                              |
| [**Subclases \_**](swbemobject-subclasses-.md)               | Devuelve una colección de subclases del objeto (que debe ser una clase WMI).<br/>                |
| [**SubclassesAsync\_**](swbemobject-subclassesasync-.md)     | Devuelve de forma asincrónica una colección de subclases del objeto (que debe ser una clase WMI).<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemObject** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso          | Descripción                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Derivación\_**](swbemobject-derivation-.md)<br/> | Solo lectura<br/> | Contiene una matriz de cadenas que describe la jerarquía de derivación de la clase.<br/>                                             |
| [**Métodos\_**](swbemobject-methods-.md)<br/>       | Solo lectura<br/> | Un objeto [**SWbemMethodSet**](swbemmethodset.md) que es la colección de métodos para este objeto.<br/>                           |
| [**Ruta\_**](swbemobject-path-.md)<br/>             | Solo lectura<br/> | Contiene un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual.<br/> |
| [**Propiedades\_**](swbemobject-properties-.md)<br/> | Solo lectura<br/> | Un objeto [**SWbemPropertySet**](swbempropertyset.md) que es la colección de propiedades de este objeto.<br/>                    |
| [**Calificadores\_**](swbemobject-qualifiers-.md)<br/> | Solo lectura<br/> | Un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que es la colección de calificadores para este objeto.<br/>                  |
| [**Seguridad\_**](swbemobject-security-.md)<br/>     | Solo lectura<br/> | Contiene un objeto [**SWbemSecurity**](swbemsecurity.md) que se usa para leer o cambiar la configuración de seguridad.<br/>                         |



 

## <a name="examples"></a>Ejemplos

La [lista de todas las propiedades y métodos de un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) ejemplo de código de VBScript de clase WMI en la galería de TechNet usa SWbemObject para enumerar todos los métodos y propiedades de una clase WMI especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

