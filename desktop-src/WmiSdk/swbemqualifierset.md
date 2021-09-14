---
description: Un objeto SWbemQualifierSet es una colección de objetos SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objeto SWbemQualifierSet (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070388"
---
# <a name="swbemqualifierset-object"></a>Objeto SWbemQualifierSet

Un **objeto SWbemQualifierSet** es una colección de [**objetos SWbemQualifier.**](swbemqualifier.md) Los elementos se agregan a la colección mediante el método [**Add,**](swbemqualifierset-add.md) se recuperan de la colección mediante el [**método Item**](swbemqualifierset-item.md) y se quitan de la colección mediante el [**método Remove.**](swbemqualifierset-remove.md) La llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

Para obtener más información, vea [Accessing a Collection](accessing-a-collection.md).

Los [**objetos SWbemQualifier**](swbemqualifier.md) que son una colección **SWbemQualifierSet** describen los calificadores asociados a un parámetro de clase, instancia, método o método WMI.

## <a name="members"></a>Members

El **objeto SWbemQualifierSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemQualifierSet** tiene estos métodos.



| Método                                     | Descripción                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Añadir**](swbemqualifierset-add.md)       | Agrega un [**objeto SWbemQualifier**](swbemqualifier.md) a la **colección SWbemQualifierSet.**<br/> |
| [**Artículo**](swbemqualifierset-item.md)     | Devuelve un objeto [**SWbemQualifier con nombre**](swbemqualifier.md) de la colección.<br/>             |
| [**Remove**](swbemqualifierset-remove.md) | Elimina un calificador con nombre de la colección.<br/>                                                   |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemQualifierSet** tiene estas propiedades.



| Propiedad.                                            | Tipo de acceso          | Descripción                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**Contar**](swbemqualifierset-count.md)<br/> | Solo lectura<br/> | Contiene el número de elementos de una **colección SWbemQualifierSet.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




