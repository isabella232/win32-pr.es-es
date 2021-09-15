---
description: Un objeto SWbemPropertySet es una colección de objetos SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objeto SWbemPropertySet (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567221"
---
# <a name="swbempropertyset-object"></a>Objeto SWbemPropertySet

Un **objeto SWbemPropertySet** es una colección de [**objetos SWbemProperty.**](swbemproperty.md) Puede agregar elementos a la colección mediante el método [**Add,**](swbempropertyset-add.md) recuperar elementos de la colección mediante el [**método Item**](swbempropertyset-item.md) y quitar elementos de la colección mediante el [**método Remove.**](swbempropertyset-remove.md) Para obtener más información, vea [Acceso a una colección](accessing-a-collection.md). La llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

Los [**objetos SWbemProperty que**](swbemproperty.md) son una colección **SWbemPropertySet** se usan para describir las propiedades de una única clase o instancia de WMI.

## <a name="members"></a>Members

El **objeto SWbemPropertySet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemPropertySet** tiene estos métodos.



| Método                                    | Descripción                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Añadir**](swbempropertyset-add.md)       | Agrega un [**objeto SWbemProperty a**](swbemproperty.md) la **colección SWbemPropertySet.**<br/>                        |
| [**Elemento**](swbempropertyset-item.md)     | Obtiene un [**objeto SWbemProperty con nombre**](swbemproperty.md) de la colección. Este es el método predeterminado para este objeto .<br/> |
| [**Quitar**](swbempropertyset-remove.md) | Elimina un [**objeto SWbemProperty**](swbemproperty.md) de la colección.<br/>                                        |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemPropertySet** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Contar**](swbempropertyset-count.md)<br/> | Solo lectura<br/> | Número de elementos de la **colección SWbemPropertySet.**<br/> |



 

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript siguiente se muestra cómo [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) puede devolver **wbemErrResetToDefault** si se invalida la propiedad .


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPropertySet<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemPropertySet<br/>                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 




