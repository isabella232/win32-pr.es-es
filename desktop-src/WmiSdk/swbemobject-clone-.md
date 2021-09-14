---
description: El método \_ Clone del objeto SWbemObject devuelve un nuevo objeto que es un clon del objeto actual.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: SWbemObject.Clone_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967072"
---
# <a name="swbemobjectclone_-method"></a>Método SWbemObject.Clone \_

El **\_ método Clone** del [**objeto SWbemObject**](swbemobject.md) devuelve un nuevo objeto que es un clon del objeto actual.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve un [**nuevo objeto SWbemObject.**](swbemobject.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ Clone,** el **objeto Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

**No** se especificó nada como parámetro y no es aceptable en este uso.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para clonar el objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el **método Clone \_** para duplicar una definición de clase o una instancia de . Esto resulta útil cuando se necesita la copia original del objeto con fines de copia de seguridad mientras se modifica una nueva copia. Del mismo modo, use este método para crear muchas instancias nuevas a partir de una única instancia de origen. Por ejemplo, use [**SWbemObject.SpawnInstance \_**](swbemobject-spawninstance-.md) para crear una instancia inicial única y **SWbemObject.Clone \_** para generar 100 copias de la instancia rápidamente. Posteriormente, puede modificar los objetos, dando a cada uno valores específicos.

No es posible usar este método para convertir una definición de clase en una instancia de o para convertir una instancia en una definición de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




