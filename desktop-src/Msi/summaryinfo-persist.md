---
description: El método Persist de los formatos de objeto SummaryInfo y escribe las propiedades previamente almacenadas en el flujo SummaryInformation estándar.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. Persist (método)
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
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680434"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo. Persist (método)

El método **Persist** de los formatos de objeto [**SummaryInfo**](summaryinfo-object.md) y escribe las propiedades previamente almacenadas en el flujo SummaryInformation estándar. Genera un error si la secuencia no se puede escribir correctamente. Solo se puede llamar una vez a este método una vez que se han establecido todos los valores de propiedad. Todavía se pueden leer las propiedades después de escribir la secuencia.

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
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




