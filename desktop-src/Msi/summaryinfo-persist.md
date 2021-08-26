---
description: El método Persist del objeto SummaryInfo da formato y escribe las propiedades almacenadas anteriormente en la secuencia SummaryInformation estándar.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Método SummaryInfo.Persist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039605"
---
# <a name="summaryinfopersist-method"></a>Método SummaryInfo.Persist

El **método Persist** del objeto [**SummaryInfo**](summaryinfo-object.md) da formato y escribe las propiedades almacenadas anteriormente en la secuencia SummaryInformation estándar. Genera un error si la secuencia no se puede escribir correctamente. Solo se puede llamar a este método una vez después de establecer todos los valores de propiedad. Las propiedades todavía se pueden leer después de escribir la secuencia.

## <a name="syntax"></a>Sintaxis


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISummaryInfo se define como \_ 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




