---
description: La propiedad Property del objeto SummaryInfo establece u obtiene el valor de la propiedad especificada en el flujo de información de resumen.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo.Property, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b8635d081b44adfad3b3e869cb7fab96ee3d81107a8d962153f1caa5a14ac72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624102"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo.Property, propiedad

La **propiedad Property** del objeto [**SummaryInfo**](summaryinfo-object.md) establece u obtiene el valor de la propiedad especificada en el flujo de información de resumen. Las propiedades se leen cuando se crea el objeto [**SummaryInfo,**](summaryinfo-object.md) pero no se escriben hasta que se llama [**al método Persist.**](summaryinfo-persist.md) Establecer una propiedad en Empty provoca su eliminación; Del mismo modo, la solicitud de una propiedad inexistente devuelve un valor Vacío. De lo contrario, los valores se pueden transferir como cadenas, enteros o tipos de fecha (fecha y hora).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valor de propiedad

Identificador de propiedad requerido de una de las propiedades de resumen.

## <a name="remarks"></a>Observaciones

**IDs de propiedad de resumen estándar**

(no una enumeración)



| Nombre de parámetro     | Value | Descripción                                       |
|--------------------|-------|---------------------------------------------------|
| DICCIONARIO \_ PID    | 0     | Formato especial, no compatible con el objeto SummaryInfo |
| PÁGINA \_ DE CÓDIGOS PID      | 1     | VT \_ I2                                            |
| TÍTULO \_ DE PID         | 2     | VT \_ LPSTR                                         |
| ASUNTO DEL \_ PID       | 3     | VT \_ LPSTR                                         |
| AUTOR DE \_ PID        | 4     | VT \_ LPSTR                                         |
| PALABRAS \_ CLAVE PID      | 5     | VT \_ LPSTR                                         |
| COMENTARIOS \_ DE PID      | 6     | VT \_ LPSTR                                         |
| PLANTILLA \_ DE PID      | 7     | VT \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT \_ LPSTR                                         |
| PID \_ EDITTIME      | 10    | VT \_ FILETIME                                      |
| PID \_ LASTPRINTED   | 11    | VT \_ FILETIME                                      |
| PID \_ CREATE \_ DTM   | 12    | VT \_ FILETIME                                      |
| PID \_ LASTSAVE \_ DTM | 13    | VT \_ FILETIME                                      |
| PID \_ PAGECOUNT     | 14    | VT \_ I4                                            |
| PID \_ WORDCOUNT     | 15    | VT \_ I4                                            |
| PID \_ CHARCOUNT     | 16    | VT \_ I4                                            |
| MINIATURA DE \_ PID     | 17    | VT \_ CF (no compatible)                            |
| PID \_ APPNAME       | 18    | VT \_ LPSTR                                         |
| SEGURIDAD DE \_ PID      | 19    | VT \_ I4                                            |



 

**Tipos de datos de las propiedades**

(no una enumeración)



| Nombre de parámetro | Value | Descripción                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | Entero de 16 bits                                                                           |
| VT \_ I4         | 3     | Entero de 32 bits                                                                           |
| VT \_ LPSTR      | 30    | String                                                                                   |
| VT \_ FILETIME   | 64    | Fecha y hora (FILETIME, convertida en hora variant)                                          |
| VT \_ CF         | 71    | Formato del Portapapeles + datos, no manipulados por [**el objeto SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISummaryInfo se define como \_ 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




