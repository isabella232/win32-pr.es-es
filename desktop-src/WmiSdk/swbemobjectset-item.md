---
description: El método Item del objeto SWbemObjectSet obtiene un objeto SWbemObject de la colección.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Método SWbemObjectSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857225"
---
# <a name="swbemobjectsetitem-method"></a>Método SWbemObjectSet.Item

El **método Item** del objeto [**SWbemObjectSet**](swbemobjectset.md) obtiene un objeto [**SWbemObject**](swbemobject.md) de la colección.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obligatorio. Ruta de acceso relativa del objeto que se recupera de la colección. Ejemplo: Win32 \_ LogicalDisk="C:"

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve el objeto [**SWbemObject**](swbemobject.md) solicitado.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Item,** el **objeto Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrNotFound** : 2147749890 (0x80041002)
</dt> <dd>

No se encontró el elemento solicitado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **método Item** puede requerir mucho tiempo de procesador porque la enumeración completa por parte del proveedor de los elementos del conjunto es necesaria para devolver el resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




