---
description: La propiedad ComponentPath es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de la clave del componente es una clave del Registro, se devuelve la clave del Registro.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer.ComponentPath, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171726"
---
# <a name="installercomponentpath-property"></a>Installer.ComponentPath, propiedad

La **propiedad ComponentPath** es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de la clave del componente es una clave del Registro, se devuelve la clave del Registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si el componente es una clave del Registro, las raíces del registro se representan numéricamente. Por ejemplo, una ruta de acceso del Registro de "HKEY CURRENT USER SOFTWARE Microsoft" se devolvería como \_ \_ \\ \\ "01: \\ SOFTWARE \\ Microsoft". Las raíces del registro devueltas se definen de la siguiente manera:



| Root                    | Valor devuelto |
|-------------------------|----------------|
| RAÍZ DE CLASES HKEY \_ \_     | 00             |
| USUARIO ACTUAL DE HKEY \_ \_     | 01             |
| HKEY \_ LOCAL \_ MACHINE    | 02             |
| USUARIOS DE \_ HKEY             | 03             |
| HKEY \_ PERFORMANCE \_ DATA | 04             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




