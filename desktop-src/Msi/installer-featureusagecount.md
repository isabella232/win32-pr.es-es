---
description: La propiedad FeatureUsageCount es una propiedad de solo lectura que devuelve el número de veces que se ha utilizado la característica.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Propiedad Installer. FeatureUsageCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653344"
---
# <a name="installerfeatureusagecount-property"></a>Propiedad Installer. FeatureUsageCount

La propiedad **FeatureUsageCount** es una propiedad de solo lectura que devuelve el número de veces que se ha utilizado la característica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El uso de los métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o sus equivalentes de API en la característica especificada incrementa esta propiedad.

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

 

 




