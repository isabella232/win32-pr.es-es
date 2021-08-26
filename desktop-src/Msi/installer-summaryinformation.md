---
description: La propiedad SummaryInformation del objeto Installer devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades al flujo de información de resumen de un paquete o transformación.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Installer.SummaryInformation, propiedad
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
ms.openlocfilehash: f671a5424e1008787443a13f2b72e75cb931da2f0783681c360a1b03ad640aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043625"
---
# <a name="installersummaryinformation-property"></a>Installer.SummaryInformation, propiedad

La **propiedad SummaryInformation** del objeto [**Installer**](installer-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades al flujo de información de resumen de un paquete o transformación.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Si se usa un valor de *maxProperties* mayor que 0 para abrir un flujo de información de resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto. Si no lo hace, se pierde la información de flujo existente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




