---
description: La propiedad FeatureUsageDate es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Propiedad Installer. FeatureUsageDate
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
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653340"
---
# <a name="installerfeatureusagedate-property"></a>Propiedad Installer. FeatureUsageDate

La propiedad **FeatureUsageDate** es una propiedad de solo lectura que devuelve la fecha en que se usó por última vez la característica especificada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El uso de los métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o sus equivalentes de API en la característica especificada establece esta propiedad.

La fecha está en el formato de fecha de MS-DOS, tal como se muestra en la tabla siguiente.



| Bits | Contenido                                            |
|------|-----------------------------------------------------|
| 0-4  | Día del mes (1-31)                             |
| 5-8  | Mes (1 = enero, 2 = febrero, etc.)        |
| 9-15 | Desplazamiento de año desde 1980 (agregue 1980 para obtener el año real) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




