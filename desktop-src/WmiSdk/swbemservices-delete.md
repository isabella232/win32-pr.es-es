---
description: Elimina la clase o instancia que se especifica en la ruta de acceso del objeto. Solo se pueden eliminar objetos en el espacio de nombres actual.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Método SWbemServices. Delete (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497836"
---
# <a name="swbemservicesdelete-method"></a>SWbemServices. Delete (método)

El método **Delete** del objeto [**SWbemServices**](swbemservices.md) elimina la clase o la instancia que se especifica en la ruta de acceso del objeto. Solo se pueden eliminar objetos en el espacio de nombres actual.

Si un proveedor dinámico proporciona la clase o la instancia, no se puede eliminar este objeto a menos que el proveedor admita la eliminación de la clase o la instancia.

Se llama a este método en el modo sincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Cadena que contiene la ruta de acceso al objeto que desea eliminar. Para obtener más información, vea [Descripción de la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Reservado. Este valor debe ser cero.

</dd> <dt>

*objWbemNamedValueSet* \[ opta\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Delete** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El contexto actual no tiene los derechos de seguridad adecuados para eliminar el objeto.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La clase especificada no existe.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

No se puede eliminar el objeto.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

El objeto no existe.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método **SWbemServices. Delete** se puede usar cuando la propiedad de clave del objeto no tiene un valor, porque este método solo requiere una ruta de acceso de objeto como entrada. Este método se puede usar en situaciones en las que se produce un error en [**SWbemObject. Delete \_**](swbemobject-delete-.md) por falta de un valor de clave. Si el objeto se confirma en WMI a través de [**SWbemObject \_ . put**](swbemobject-put-.md), se obtuvo un objeto [**SWbemObjectPath**](swbemobjectpath.md) a través de la llamada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una nueva clase, se agrega una propiedad que no es una clave, se escribe la nueva clase en el repositorio y se muestra la ruta de acceso del nuevo objeto de clase. A continuación, el script genera una instancia de la nueva clase, escribe la instancia y muestra la ruta de acceso. Tenga en cuenta que el script elimina la clase y sus instancias del repositorio mediante la eliminación de la clase. Para obtener más información sobre las clases e instancias de WMI, vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md) y [modelo de información común](common-information-model.md).


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

 




