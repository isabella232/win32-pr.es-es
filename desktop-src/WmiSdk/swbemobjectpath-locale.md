---
description: La propiedad locale del objeto SWbemObjectPath contiene la configuración regional de la ruta de acceso del objeto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Locale (Wbemdisp. h)
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
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697358"
---
# <a name="swbemobjectpathlocale-property"></a>Propiedad SWbemObjectPath. Locale

La propiedad **locale** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene la configuración regional de la ruta de acceso del objeto.

Cuando la propiedad **SWbemObjectPath. Locale** forma parte de un objeto [**SWbemObjectPath**](swbemobjectpath.md) independiente, es de lectura y escritura y se puede usar para establecer el componente de configuración regional del moniker.

Cuando se tiene acceso a la propiedad **SWbemObjectPath. Locale** como parte de una propiedad [**SWbemObject \_ . Path**](swbemobject-path-.md) , es de solo lectura y notifica el valor de la configuración regional que se usa para enlazar con el espacio de nombres desde el que se obtuvo el objeto.

En el caso de los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS \_ xxxx", donde XXXX es una cadena en formato hexadecimal que indica el LCID. Por ejemplo, el identificador de configuración regional de Inglés de Estados Unidos es "MS \_ 409".

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                        |



 

 




