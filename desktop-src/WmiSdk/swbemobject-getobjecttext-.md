---
description: El método GetObjectText \_ del objeto SWbemObject devuelve una representación textual del objeto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: SWbemObject.GetObjectText_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d33e4f3f530bf7d9bda2e228243026de7d3768efb668cf6c8683690e8127f65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992065"
---
# <a name="swbemobjectgetobjecttext_-method"></a>Método SWbemObject.GetObjectText \_

El **método \_ GetObjectText** del [**objeto SWbemObject**](swbemobject.md) devuelve una representación textual del objeto. Este objeto se puede usar para mostrar el contenido de un objeto. Actualmente, solo se admite la sintaxis MOF como formato de salida. Observe que el texto MOF devuelto no contiene toda la información sobre el objeto; El texto MOF contiene solo información suficiente para que el compilador MOF pueda volver a crear el objeto original. Por ejemplo, no hay información sobre los calificadores propagados o las propiedades de clase primaria.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Reservado y debe ser 0 (cero) si se especifica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve una cadena que contiene el texto de salida.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método \_ GetObjectText,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

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

</dd> </dl>

## <a name="examples"></a>Ejemplos

El código siguiente, tomado del ejemplo de código [LIST the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript de la Galería de TechNet, recupera y muestra la representación textual de una definición de clase WMI en la sintaxis MOF (Managed Object Format).


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



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



 

 




