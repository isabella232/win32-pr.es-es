---
description: La propiedad ProductInfo es una propiedad de solo lectura que devuelve el valor del atributo especificado para un producto instalado o publicado.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Propiedad Installer. ProductInfo (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653954"
---
# <a name="installerproductinfo-property"></a>Installer. ProductInfo (propiedad)

La propiedad **ProductInfo** es una propiedad de solo lectura que devuelve el valor del atributo especificado para un producto instalado o publicado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

La propiedad **ProductInfo** ("LocalPackage") no devuelve necesariamente una ruta de acceso al paquete almacenado en caché. No se deben invocar las instalaciones del modo de mantenimiento desde LocalPackage. El paquete en caché solo es para uso interno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Encabezado<br/>  | <dl> <dt>Oemupgex. h</dt> </dl>                                                                                                                                                                                 |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




