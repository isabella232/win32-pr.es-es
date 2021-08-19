---
description: El método Clone del objeto SWbemLastError devuelve un nuevo objeto que es \_ un clon del objeto SWbemLastError actual.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: SWbemLastError.Clone_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314671"
---
# <a name="swbemlasterrorclone_-method"></a>Método SWbemLastError.Clone \_

El **\_ método Clone** del [**objeto SWbemLastError**](swbemlasterror.md) devuelve un nuevo objeto que es un clon del objeto **SWbemLastError** actual.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el **método Clone \_** se realiza correctamente, devuelve un nuevo objeto [**SWbemLastError.**](swbemlasterror.md)

## <a name="error-codes"></a>Códigos de error

Tras la finalización del método **\_ Clone,** el **objeto Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use el **método Clone \_** para duplicar una instancia o definición de clase. Este método es útil cuando necesita hacer una copia de seguridad de la copia original del objeto mientras modifica una nueva copia. Además, use este método para crear muchas instancias nuevas a partir de una única instancia de origen. Por ejemplo, use [**SWbemObject.SpawnInstance \_**](swbemobject-spawninstance-.md) para crear una instancia inicial única y **use SWbemLastError.Clone \_** para generar 100 copias de la instancia rápidamente. Posteriormente, puede modificar los objetos, dando valores específicos a cada objeto.

No es posible usar este método para convertir una definición de clase en una instancia o convertir una instancia en una definición de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




