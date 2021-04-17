---
description: La propiedad ComponentPath es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de la clave para el componente es una clave del registro, se devuelve la clave del registro.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Propiedad Installer. ComponentPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653694"
---
# <a name="installercomponentpath-property"></a>Propiedad Installer. ComponentPath

La propiedad **ComponentPath** es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de la clave para el componente es una clave del registro, se devuelve la clave del registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si el componente es una clave del registro, las raíces del registro se representan numéricamente. Por ejemplo, una ruta de acceso del registro "HKEY \_ Current \_ User \\ software \\ Microsoft" se devolverá como "01: \\ software \\ Microsoft". Las raíces del registro devueltas se definen de la siguiente manera:



| Root                    | Valor devuelto |
|-------------------------|----------------|
| \_clase HKEY \_ raíz     | 00             |
| HKEY \_ Current \_ User     | 01             |
| HKEY \_ local \_ Machine    | 02             |
| \_usuarios HKEY             | 03             |
| \_datos de rendimiento de HKEY \_ | 04             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




