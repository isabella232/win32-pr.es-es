---
description: La propiedad ColumnInfo del objeto View devuelve un objeto Record que contiene la información solicitada sobre cada columna del conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View.ColumnInfo, propiedad
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
ms.openlocfilehash: 08996c3e77212032eac8f65621c7f8ca9ee8489683295c63fb30092995ad41d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012713"
---
# <a name="viewcolumninfo-property"></a>View.ColumnInfo, propiedad

La **propiedad ColumnInfo** del [**objeto View**](view-object.md) devuelve un objeto [**Record**](record-object.md) que contiene la información solicitada sobre cada columna del conjunto de resultados. Se pueden solicitar los nombres de columna o las definiciones de columna. Las constantes proporcionadas en la lista Seleccionar no tienen nombres.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valor de propiedad

Información necesaria para cada columna.



| Nombre de parámetro                                                                                                                                                                                                                                                          | Significado                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Devuelve los nombres de todas las columnas no dependientes del conjunto de resultados.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Devuelve los tipos de todas las columnas no compatibles del conjunto de resultados.<br/> |



 

## <a name="remarks"></a>Comentarios

Las descripciones de columna devueltas por **la propiedad ColumnInfo** tienen el formato descrito en [Formato de definición de columna](column-definition-format.md). Cada columna se describe mediante una cadena en el campo de registro correspondiente. La cadena de definición consta de una sola letra que representa el tipo de datos seguido del ancho de la columna (en caracteres cuando corresponda, o bien bytes). Un ancho de cero designa un ancho sin enlazar (campos de texto largos y secuencias). Una letra mayúscula indica que se permiten valores NULL en la columna.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView se define como \_ 000C109C-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



 

 




