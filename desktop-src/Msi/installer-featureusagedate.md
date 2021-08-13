---
description: La propiedad FeatureUsageDate es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer.FeatureUsageDate, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15c628b95f6dab2d671e660c9783e071e1e4385c165363fdf9ad39abd571510e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631072"
---
# <a name="installerfeatureusagedate-property"></a>Installer.FeatureUsageDate, propiedad

La **propiedad FeatureUsageDate** es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El uso de [**los métodos UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o sus equivalentes de API en la característica especificada establece esta propiedad.

La fecha tiene el formato de fecha MS-DOS, como se muestra en la tabla siguiente.



| Bits | Contenido                                            |
|------|-----------------------------------------------------|
| 0-4  | Día del mes (1-31)                             |
| 5-8  | Mes (1 = enero, 2 = febrero, y así sucesivamente)        |
| 9-15 | Desplazamiento del año desde 1980 (agregar 1980 para obtener el año real) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




