---
description: El método FeatureInfo del objeto de sesión devuelve un objeto FeatureInfo que contiene información descriptiva de la característica especificada.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Método Session. FeatureInfo
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
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653827"
---
# <a name="sessionfeatureinfo-method"></a>Método Session. FeatureInfo

El método **FeatureInfo** del objeto de [**sesión**](session-object.md) devuelve un objeto **FeatureInfo** que contiene información descriptiva de la característica especificada.

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



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




