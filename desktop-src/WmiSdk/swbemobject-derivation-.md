---
description: La propiedad Derivation del objeto SWbemObject contiene una matriz de cadenas que describen la jerarquía de derivación de clases para la instancia a la \_ que se hace referencia.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: SWbemObject.Derivation_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 35195a6e3067fa68db747f04df8ec2c70480d297e4780c48059a1ba7f031e453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313907"
---
# <a name="swbemobjectderivation_-property"></a>Propiedad SWbemObject.Derivation \_

La **propiedad \_ Derivation** del objeto [**SWbemObject**](swbemobject.md) contiene una matriz de cadenas que describen la jerarquía de derivación de clases para la instancia a la que se hace referencia. El primer elemento de la matriz define la clase primaria y el último elemento define la clase Deserción. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript siguiente se describe cómo recuperar la jerarquía de clases para win32 \_ logicaldisk.


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



Siguiendo el ejemplo de Perl se describe cómo recuperar la jerarquía de clases para win32 \_ logicaldisk.


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
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



 

 




