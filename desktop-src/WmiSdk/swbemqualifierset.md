---
description: Un objeto SWbemQualifierSet es una colección de objetos SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objeto SWbemQualifierSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083380"
---
# <a name="swbemqualifierset-object"></a>Objeto SWbemQualifierSet

Un objeto **SWbemQualifierSet** es una colección de objetos [**SWbemQualifier**](swbemqualifier.md) . Los elementos se agregan a la colección mediante el método [**Add**](swbemqualifierset-add.md) , se recuperan de la colección mediante el método [**Item**](swbemqualifierset-item.md) y se quitan de la colección mediante el método [**Remove**](swbemqualifierset-remove.md) . Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.

Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

Los objetos [**SWbemQualifier**](swbemqualifier.md) que componen una colección **SWbemQualifierSet** describen los calificadores adjuntos a una clase WMI, una instancia, un método o un parámetro de método.

## <a name="members"></a>Miembros

El objeto **SWbemQualifierSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemQualifierSet** tiene estos métodos.



| Método                                     | Descripción                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Agréguela**](swbemqualifierset-add.md)       | Agrega un objeto [**SWbemQualifier**](swbemqualifier.md) a la colección **SWbemQualifierSet** .<br/> |
| [**Elemento**](swbemqualifierset-item.md)     | Devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) con nombre de la colección.<br/>             |
| [**Retirar**](swbemqualifierset-remove.md) | Elimina un calificador con nombre de la colección.<br/>                                                   |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemQualifierSet** tiene estas propiedades.



| Propiedad                                            | Tipo de acceso          | Descripción                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Contabiliza**](swbemqualifierset-count.md)<br/> | Solo lectura<br/> | Contiene el número de elementos de una colección **SWbemQualifierSet** .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | \_ISWBEMQUALIFIERSET IID<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




