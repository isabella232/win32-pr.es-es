---
description: La propiedad SummaryInformation del objeto de instalador devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de Resumen de un paquete o transformación.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Propiedad Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653386"
---
# <a name="installersummaryinformation-property"></a>Propiedad Installer. SummaryInformation

La propiedad **SummaryInformation** del objeto de [**instalador**](installer-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de Resumen de un paquete o transformación.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si se usa un valor de *maxProperties* mayor que 0 para abrir una secuencia de información de Resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto. Si no lo hace, se pierde la información de la secuencia existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




