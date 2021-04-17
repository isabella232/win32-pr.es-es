---
description: La propiedad Datasize del objeto Record es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propiedad record. Datasize
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653676"
---
# <a name="recorddatasize-property"></a>Propiedad record. Datasize

La propiedad **datasize** del objeto [**Record**](record-object.md) es una propiedad de solo lectura que devuelve el tamaño de los datos del campo designado. Si los datos son una secuencia, se devuelve la longitud de la secuencia en bytes. Si los datos son una cadena, se devuelve la longitud de la cadena sin null. Si los datos son un entero, se devuelve el valor 4 (que indica el tamaño del entero). Si los datos son NULL, se devuelve 0.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valor de propiedad

Número de campo obligatorio del valor dentro del registro, basado en 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




