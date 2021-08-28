---
description: Use el método SpawnInstance \_ del objeto SWbemObject para crear una nueva instancia de una clase.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: SWbemObject.SpawnInstance_ método (Wbemdisp.h)
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
ms.openlocfilehash: 1b465bb53fd031dff397ef0ddf39db39d5d9987f03e037becebcd8dd41a65b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640045"
---
# <a name="swbemobjectspawninstance_-method"></a>Método SWbemObject.SpawnInstance \_

Use el **método SpawnInstance \_** del objeto [**SWbemObject**](swbemobject.md) para crear una nueva instancia de una clase. El objeto actual debe ser una definición de clase obtenida de WMI a través de un método como [**SWbemServices.Get**](swbemservices-get.md) [**oSWbemServices.ExecQuery**](swbemservices-execquery.md). A continuación, use esta definición de clase para crear nuevas instancias. Cree cada nueva instancia localmente dentro del proceso y, a continuación, llame a [**SWbemObject.Put \_**](swbemobject-put-.md) para crear realmente la instancia dentro de WMI.

> [!Note]  
> Se admite la generación de una instancia de a partir de una instancia de , pero la instancia devuelta está vacía.

 

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Reservado y debe ser cero si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta llamada devuelve [**un objeto SWbemObject**](swbemobject.md) que contiene una nueva instancia de la clase .

## <a name="error-codes"></a>Códigos de error

Después de completar el método **SpawnInstance, \_** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrIncompleteClass:** 2147749920 (0x80041020)
</dt> <dd>

El objeto actual no es una definición de clase válida y no puede generar nuevas instancias. O bien está incompleta o no se ha registrado con WMI mediante [**SWbemObject.Put \_**](swbemobject-put-.md).

</dd> <dt>

**wbemErrGallgalOperation:** 2147749918 (0x8004101E)
</dt> <dd>

Se devuelve si este método se usa en una instancia en lugar de en una clase.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

 




