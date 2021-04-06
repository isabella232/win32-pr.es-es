---
description: El \_ método GetObjectText del objeto SWbemLastError devuelve una representación textual del objeto en un formato Managed Object Format (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Método SWbemLastError.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002121"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>SWbemLastError. GetObjectText, \_ método

El **método \_ GetObjectText** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve una representación textual del objeto en un formato [Managed Object Format (MOF)](managed-object-format--mof-.md) . Este objeto MOF se puede usar para mostrar el contenido de un objeto. Observe que el texto MOF que se devuelve no contiene toda la información sobre el objeto, sino solo información suficiente para que el compilador MOF pueda volver a crear el objeto original. Por ejemplo, no encontrará información sobre los calificadores propagados o las propiedades de la clase primaria.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Este parámetro está reservado y debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, este método devuelve una cadena que contiene el texto de salida.

## <a name="error-codes"></a>Códigos de error

Una vez finalizado el **método \_ GetObjectText** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Un parámetro especificado no es válido.

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
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



 

 




