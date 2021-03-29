---
description: El método UseFeature del objeto instalador incrementa el recuento de uso de una característica determinada y devuelve el estado de la instalación de esa característica. Este método se debe usar para indicar que la intención de una aplicación es usar una característica.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Instalador. UseFeature (método)
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
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653886"
---
# <a name="installerusefeature-method"></a>Instalador. UseFeature (método)

El método **UseFeature** del objeto [**instalador**](installer-object.md) incrementa el recuento de uso de una característica determinada y devuelve el estado de la instalación de esa característica. Este método se debe usar para indicar que la intención de una aplicación es usar una característica.

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

Este parámetro debe ser *msiInstallModeNoDetection*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **UseFeature** solo debe usarse en las características que se sabe que se van a publicar. La aplicación debe determinar el estado de la característica mediante una llamada a la propiedad [**FeatureState**](installer-featurestate.md) o a la propiedad [**características**](installer-features.md) , o a sus equivalentes de API.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




