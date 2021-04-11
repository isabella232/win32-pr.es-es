---
description: Use el \_ método SpawnDerivedClass del objeto SWbemObject para crear un objeto de clase derivada a partir del objeto actual. El objeto debe ser una definición de clase que se convierte en la clase primaria del objeto generado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Método SWbemObject.SpawnDerivedClass_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276126"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>SWbemObject. SpawnDerivedClass, \_ método

Use el **método \_ SpawnDerivedClass** del objeto [**SWbemObject**](swbemobject.md) para crear un objeto de clase derivada a partir del objeto actual. El objeto debe ser una definición de clase que se convierte en la clase primaria del objeto generado.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ opta\]
</dt> <dd>

Reserved y debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, el objeto [**SWbemObject**](swbemobject.md) contiene el nuevo objeto de definición de clase. No se devuelve ningún objeto cuando se produce un error.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **SpawnDerivedClass \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

El usuario solicitó una operación no válida, como generar una clase a partir de una instancia.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

La clase de origen no se definió por completo ni se registró en WMI, por lo que no se permite una nueva clase derivada.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El objeto que se devuelve automáticamente se convierte en una subclase del objeto actual. Este comportamiento no se puede invalidar. No hay ningún otro método por el que pueda crear clases derivadas.

No se puede crear una clase derivada a partir de una clase que sea local para su propio proceso de cliente. Antes de utilizar este método para crear una clase derivada, debe crear la clase base. Para crear la clase base, llame a [**SWbemObject. \_ Put**](swbemobject-put-.md)y recupere la clase base mediante [**SWbemServices. Get**](swbemservices-get.md).

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



 

 




