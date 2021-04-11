---
description: Use el \_ método SpawnInstance del objeto SWbemObject para crear una nueva instancia de una clase.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Método SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279106"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject. SpawnInstance, \_ método

Use el **método \_ SpawnInstance** del objeto [**SWbemObject**](swbemobject.md) para crear una nueva instancia de una clase. El objeto actual debe ser una definición de clase obtenida de WMI a través de un método como [**SWbemServices. Get**](swbemservices-get.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md). A continuación, use esta definición de clase para crear nuevas instancias. Cree cada nueva instancia localmente en el proceso y, a continuación, llame a [**SWbemObject. put \_**](swbemobject-put-.md) para crear realmente la instancia en WMI.

> [!Note]  
> Se admite la generación de una instancia a partir de una instancia de, pero la instancia devuelta está vacía.

 

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reserved y debe ser cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta llamada devuelve un objeto [**SWbemObject**](swbemobject.md) que contiene una nueva instancia de la clase.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **SpawnInstance \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

El objeto actual no es una definición de clase válida y no puede generar nuevas instancias. O bien está incompleto o no se ha registrado con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101E)
</dt> <dd>

Se devuelve si este método se usa en una instancia de en lugar de en una clase.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> </dl>

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

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices. get**](swbemservices-get.md)
</dt> </dl>

 

 




