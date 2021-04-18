---
description: La propiedad Property del objeto SummaryInfo establece u obtiene el valor de la propiedad especificada en la secuencia de información de resumen.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo. Property (propiedad)
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
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679453"
---
# <a name="summaryinfoproperty-property"></a>SummaryInfo. Property (propiedad)

La propiedad **Property** del objeto [**SummaryInfo**](summaryinfo-object.md) establece u obtiene el valor de la propiedad especificada en la secuencia de información de resumen. Las propiedades se leen cuando se crea el objeto [**SummaryInfo**](summaryinfo-object.md) , pero no se escriben hasta que se llama al método [**Persist**](summaryinfo-persist.md) . Establecer una propiedad en Empty provoca su eliminación; del mismo modo, si se solicita una propiedad inexistente, se devuelve un valor vacío. De lo contrario, los valores se pueden transferir como cadenas, enteros o tipos de fecha (fecha y hora).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valor de propiedad

IDENTIFICADOR de propiedad obligatorio de una de las propiedades de resumen.

## <a name="remarks"></a>Observaciones

**Identificadores de propiedad de Resumen estándar**

(no una enumeración)



| Nombre de parámetro     | Value | Descripción                                       |
|--------------------|-------|---------------------------------------------------|
| Diccionario de PID \_    | 0     | Formato especial, no compatible con el objeto SummaryInfo |
| Página de códigos de PID \_      | 1     | I2 de VT \_                                            |
| Título del PID \_         | 2     | VT \_ LPSTR                                         |
| asunto del PID \_       | 3     | VT \_ LPSTR                                         |
| autor del PID \_        | 4     | VT \_ LPSTR                                         |
| \_palabras clave de PID      | 5     | VT \_ LPSTR                                         |
| Comentarios de PID \_      | 6     | VT \_ LPSTR                                         |
| plantilla de PID \_      | 7     | VT \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT \_ LPSTR                                         |
| PID \_ EDITTIME      | 10    | VT \_ FILETIME                                      |
| PID \_ LASTPRINTED   | 11    | VT \_ FILETIME                                      |
| PID \_ Create \_ DTM   | 12    | VT \_ FILETIME                                      |
| PID \_ LASTSAVE \_ DTM | 13    | VT \_ FILETIME                                      |
| PID \_ PAGECOUNT     | 14    | VT \_ I4                                            |
| PID \_ WORDCOUNT     | 15    | VT \_ I4                                            |
| CHARCOUNT de PID \_     | 16    | VT \_ I4                                            |
| miniatura de PID \_     | 17    | VT \_ CF (no compatible)                            |
| PID \_ APPNAME       | 18    | VT \_ LPSTR                                         |
| seguridad de PID \_      | 19    | VT \_ I4                                            |



 

**Tipos de datos de las propiedades**

(no una enumeración)



| Nombre de parámetro | Value | Descripción                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| I2 de VT \_         | 2     | Entero de 16 bits                                                                           |
| VT \_ I4         | 3     | Entero de 32 bits                                                                           |
| VT \_ LPSTR      | 30    | String                                                                                   |
| VT \_ FILETIME   | 64    | Fecha y hora (FILETIME, convertido a la hora de variante)                                          |
| VT \_ CF         | 71    | Formato del portapapeles + datos, no administrados por el objeto [**SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




