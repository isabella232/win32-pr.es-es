---
description: Use el método SpawnDerivedClass del \_ objeto SWbemObject para crear un objeto de clase derivada a partir del objeto actual. El objeto debe ser una definición de clase que se convierta en la clase primaria del objeto generado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_ método (Wbemdisp.h)
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
ms.openlocfilehash: 0ed0a01926c76ecfc4d393a4de8225d7d0c98a9904f113aed18cd1cb5f8ccabb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313799"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>Método SWbemObject.SpawnDerivedClass \_

Use el **método \_ SpawnDerivedClass** del [**objeto SWbemObject**](swbemobject.md) para crear un objeto de clase derivada a partir del objeto actual. El objeto debe ser una definición de clase que se convierta en la clase primaria del objeto generado.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Reservado y debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la llamada se realiza correctamente, el [**objeto SWbemObject**](swbemobject.md) contiene el nuevo objeto de definición de clase. Ningún objeto devuelve cuando se produce un error.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **\_ SpawnDerivedClass,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErr HrgalOperation:** 2147749918 (0x8004101E)
</dt> <dd>

El usuario solicitó una operación no ilegal, como generar una clase a partir de una instancia de .

</dd> <dt>

**wbemErrIncompleteClass:** 2147749920 (0x80041020)
</dt> <dd>

La clase de origen no se definió completamente ni se registró con WMI, por lo que no se permite una nueva clase derivada.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El objeto que se devuelve automáticamente se convierte en una subclase del objeto actual. Este comportamiento no se puede invalidar. No hay ningún otro método por el que se puedan crear clases derivadas.

No puede crear una clase derivada a partir de una clase que sea local para su propio proceso de cliente. Antes de usar este método para crear una clase derivada, debe crear la clase base. Para crear la clase base, llame a [**\_ SWbemObject.Put**](swbemobject-put-.md)y recupere la clase base mediante [**SWbemServices.Get**](swbemservices-get.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




