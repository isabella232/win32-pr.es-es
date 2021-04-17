---
description: La propiedad ColumnInfo del objeto de vista devuelve un objeto de registro que contiene la información solicitada sobre cada columna del conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653551"
---
# <a name="viewcolumninfo-property"></a>View. ColumnInfo (propiedad)

La propiedad **ColumnInfo** del objeto de [**vista**](view-object.md) devuelve un objeto de [**registro**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados. Es posible que se soliciten los nombres de columna o las definiciones de columna. Las constantes que se proporcionan en la lista de selección no tienen nombres.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valor de propiedad

Información necesaria necesaria para cada columna.



| Nombre de parámetro                                                                                                                                                                                                                                                          | Significado                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Devuelve los nombres de todas las columnas no constantes en el conjunto de resultados.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Devuelve los tipos de todas las columnas no constantes en el conjunto de resultados.<br/> |



 

## <a name="remarks"></a>Observaciones

Las descripciones de columna devueltas por la propiedad **ColumnInfo** tienen el formato que se describe en [formato de definición de columna](column-definition-format.md). Cada columna se describe mediante una cadena en el campo registro correspondiente. La cadena de definición se compone de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres si es aplicable, o en bytes). Un ancho de cero designa un ancho sin enlazar (campos de texto largo y secuencias). Una letra mayúscula indica que se permiten valores NULL en la columna.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView se define como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




