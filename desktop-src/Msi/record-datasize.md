---
description: La propiedad DataSize del objeto Record es una propiedad de solo lectura que devuelve el tamaño de los datos para el campo designado.
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
ms.openlocfilehash: 067fc09e65d644413e75ccd8a9c0173e30df8060dff0f772ae5d12705ab610aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912965"
---
# <a name="recorddatasize-property"></a>Propiedad Record.DataSize

La **propiedad DataSize** del [**objeto Record**](record-object.md) es una propiedad de solo lectura que devuelve el tamaño de los datos para el campo designado. Si los datos son una secuencia, se devuelve la longitud del flujo en bytes. Si los datos son una cadena, se devuelve la longitud de cadena sin Null. Si los datos son un entero, se devuelve el valor 4 (que indica el tamaño del entero). Si los datos son Null, se devuelve 0.

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecord se define como \_ 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




