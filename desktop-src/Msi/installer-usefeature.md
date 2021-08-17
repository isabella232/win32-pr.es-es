---
description: El método UseFeature del objeto Installer incrementa el recuento de uso de una característica determinada y devuelve el estado de instalación de esa característica. Este método debe usarse para indicar la intención de una aplicación de usar una característica.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer.UseFeature (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b320ce72271bb7ee90ac85a376b103d868e6f740a2e853daf58bb478dc79ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142181"
---
# <a name="installerusefeature-method"></a>Installer.UseFeature (método)

El **método UseFeature** del objeto [**Installer**](installer-object.md) incrementa el recuento de uso de una característica determinada y devuelve el estado de instalación de esa característica. Este método debe usarse para indicar la intención de una aplicación de usar una característica.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código de producto del producto.

</dd> <dt>

*Característica* 
</dt> <dd>

Identifica la característica que se va a usar.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Este parámetro debe ser *msiInstallModeNoDetection.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **método UseFeature** solo debe usarse en características conocidas que se publican. La aplicación debe determinar el estado de la característica llamando a la propiedad [**FeatureState**](installer-featurestate.md) o [**a la propiedad Features**](installer-features.md) o a sus equivalentes de API.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




