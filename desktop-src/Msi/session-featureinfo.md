---
description: El método FeatureInfo del objeto Session devuelve un objeto FeatureInfo que contiene información descriptiva para la característica especificada.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Método Session.FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4d6e44a16305d4a46525cfed631068ff0137c642b09b8dc6a9eca169a104548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625203"
---
# <a name="sessionfeatureinfo-method"></a>Método Session.FeatureInfo

El **método FeatureInfo** del [**objeto Session**](session-object.md) devuelve un objeto **FeatureInfo** que contiene información descriptiva para la característica especificada.

## <a name="syntax"></a>Sintaxis


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Característica* 
</dt> <dd>

Identifica la característica de interés.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




