---
description: Un objeto SWbemNamedValueSet es una colección de objetos SWbemNamedValue.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Objeto SWbemNamedValueSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706055"
---
# <a name="swbemnamedvalueset-object"></a>Objeto SWbemNamedValueSet

Un objeto **SWbemNamedValueSet** es una colección de objetos [**SWbemNamedValue**](swbemnamedvalue.md) . Los métodos y las propiedades de **SWbemNamedValueSet** se usan principalmente para enviar más información a los proveedores al enviar ciertas llamadas a WMI. Todas las llamadas en [**SWbemServices**](swbemservices.md)y algunas llamadas en [**SWbemObject**](swbemobject.md)toman un parámetro opcional que es un objeto de este tipo. Un cliente puede agregar información a un objeto **SWbemNamedValueSet** y enviar el objeto **SWbemNamedValueSet** con la llamada como uno de los parámetros. Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.

Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

> [!Note]  
> Importante: si es posible, no utilice este mecanismo porque puede interrumpir el modelo de acceso uniforme que constituye la base de WMI. Si un proveedor utiliza este mecanismo, es importante que este mecanismo se use de la manera más moderada posible. Si un proveedor requiere una gran cantidad de información de contexto muy específica para responder a una solicitud, todos los clientes deben codificarse para proporcionar esta información. Este mecanismo le permite tener acceso a estos proveedores, si es necesario.

 

Un objeto **SWbemNamedValueSet** es una colección de elementos [**SWbemNamedValue**](swbemnamedvalue.md) . Estos elementos se agregan a la colección mediante el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) . Se quitan mediante el método [**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md) y se recuperan mediante el método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Puede tener acceso a los métodos para rellenar cualquier información de contexto requerida por un proveedor dinámico. Después de llamar a uno de los métodos [**SWbemServices**](swbemservices.md) , puede volver a usar el objeto **SWbemNamedValueSet** para otra llamada.

El proveedor subyacente determina la información contenida en un objeto **SWbemNamedValueSet** . WMI no hace uso de la información, sino que simplemente la reenvía al proveedor. Los proveedores deben publicar la información de contexto que requieren para atender las solicitudes.

## <a name="members"></a>Miembros

El objeto **SWbemNamedValueSet** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemNamedValueSet** tiene estos métodos.



| Método                                            | Descripción                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Agréguela**](swbemnamedvalueset-add.md)             | Agrega un objeto [**SWbemNamedValue**](swbemnamedvalue.md) a la colección.<br/>                                                  |
| [**Clonar**](swbemnamedvalueset-clone.md)         | Realiza una copia de esta colección **SWbemNamedValueSet** .<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | Quita todos los elementos de la colección, con lo que el objeto **SWbemNamedValueSet** está vacío.<br/>                                        |
| [**Elemento**](swbemnamedvalueset-item.md)           | Recupera un objeto [**SWbemNamedValue**](swbemnamedvalue.md) de la colección. Este es el método predeterminado del objeto.<br/> |
| [**Retirar**](swbemnamedvalueset-remove.md)       | Quita un objeto [**SWbemNamedValue**](swbemnamedvalue.md) de la colección.<br/>                                             |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemNamedValueSet** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso          | Descripción                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contabiliza**](swbemnamedvalueset-count.md)<br/> | Solo lectura<br/> | Número de elementos de la colección.<br/> |



 

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript muestra la manipulación de los conjuntos de valores con nombre, en el caso de que el valor con nombre sea un tipo de matriz.


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



El siguiente ejemplo de Perl muestra la manipulación de los conjuntos de valores con nombre, en el caso de que el valor con nombre sea un tipo de matriz.


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | \_ISWBEMNAMEDVALUESET IID<br/>                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 




