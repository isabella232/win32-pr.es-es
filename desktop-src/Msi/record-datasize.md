---
description: La propiedad DataSize del objeto Record es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propiedad Record.DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362315"
---
# <a name="recorddatasize-property"></a>Propiedad Record.DataSize

La **propiedad DataSize** del [**objeto Record**](record-object.md) es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado. Si los datos son una secuencia, se devuelve la longitud de la secuencia en bytes. Si los datos son una cadena, se devuelve la longitud de cadena sin null. Si los datos son un entero, se devuelve el valor 4 (que indica el tamaño del entero). Si los datos son Null, se devuelve 0.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valor de propiedad

Número de campo requerido del valor dentro del registro, basado en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-00000000046<br/>                                                                                                                                                                              |



 

 




