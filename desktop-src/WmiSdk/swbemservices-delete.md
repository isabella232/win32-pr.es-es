---
description: Elimina la clase o instancia especificada en la ruta de acceso del objeto. Solo puede eliminar objetos en el espacio de nombres actual.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Método SWbemServices.Delete (Wbemdisp.h)
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
ms.openlocfilehash: fff97be43f5689acd51b811e81d72e053f4c7ae6b4df398329016304bf418535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995655"
---
# <a name="swbemservicesdelete-method"></a>Método SWbemServices.Delete

El **método Delete** del objeto [**SWbemServices**](swbemservices.md) elimina la clase o instancia especificada en la ruta de acceso del objeto. Solo puede eliminar objetos en el espacio de nombres actual.

Si un proveedor dinámico proporciona la clase o instancia, no puede eliminar este objeto a menos que el proveedor admita la eliminación de clases o instancias.

Se llama a este método en modo sincrónico. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Obligatorio. Cadena que contiene la ruta de acceso del objeto que desea eliminar. Para obtener más información, [vea Describir la ubicación de un objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Reservado. Este valor debe ser cero.

</dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que proporciona servicios a la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Delete,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El contexto actual no tiene los derechos de seguridad adecuados para eliminar el objeto.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidClass:** 2147749904 (0x80041010)
</dt> <dd>

La clase especificada no existe.

</dd> <dt>

**wbemErrInvalidOperation:** 2147749910 (0x80041016)
</dt> <dd>

No se puede eliminar el objeto.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

El objeto no existe.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **método SWbemServices.Delete** se puede usar cuando a la propiedad de clave del objeto no se le proporciona un valor, porque este método solo requiere una ruta de acceso de objeto como entrada. Este método se puede usar en situaciones en las que se produce un error [**en SWbemObject.Delete \_**](swbemobject-delete-.md) por falta de un valor de clave. Si el objeto se confirma en WMI a través [**de SWbemObject.Put \_**](swbemobject-put-.md), se obtuvo un objeto [**SWbemObjectPath**](swbemobjectpath.md) a través de la llamada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una nueva clase, se agrega una propiedad que no es una clave, se escribe la nueva clase en el repositorio y se muestra la ruta de acceso del nuevo objeto de clase. A continuación, el script genera una instancia de la nueva clase, escribe la instancia y muestra la ruta de acceso. Tenga en cuenta que el script elimina la clase y sus instancias del repositorio mediante la eliminación de la clase . Para obtener más información sobre las clases e instancias de WMI, vea Manipular información de clase [e](manipulating-class-and-instance-information.md) instancia [y Modelo de información común](common-information-model.md).


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

 




