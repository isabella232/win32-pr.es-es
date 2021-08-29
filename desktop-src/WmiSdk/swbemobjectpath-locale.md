---
description: La propiedad Locale del objeto SWbemObjectPath contiene la configuración regional de la ruta de acceso del objeto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.Locale (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: eb9d2641aa92a4771867eef5cdd2b76d2729c3ea35a32e46d68212bf683bf2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503905"
---
# <a name="swbemobjectpathlocale-property"></a>Propiedad SWbemObjectPath.Locale

La **propiedad Locale** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene la configuración regional de la ruta de acceso del objeto.

Cuando la propiedad **SWbemObjectPath.Locale** forma parte de un objeto [**SWbemObjectPath**](swbemobjectpath.md) independiente, es de lectura y escritura y se puede usar para establecer el componente de configuración regional del moniker.

Cuando se tiene acceso a la propiedad **SWbemObjectPath.Locale** como parte de una propiedad [**SWbemObject.Path, \_**](swbemobject-path-.md) es de solo lectura e informa del valor de la configuración regional usada en el enlace al espacio de nombres del que se obtuvo el objeto.

Para los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS xxxx", donde xxxx es una cadena en formato hexadecimal que \_ indica el LCID. Por ejemplo, el identificador de configuración regional de inglés de Estados Unidos es "MS \_ 409".

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




