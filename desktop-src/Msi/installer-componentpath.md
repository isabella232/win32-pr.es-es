---
description: La propiedad ComponentPath es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de clave del componente es una clave del Registro, se devuelve la clave del Registro.
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
ms.openlocfilehash: 88601dc4c65d0d3f69a5386ed62d1523c9fa21723e73b1ad4d208d0eff437658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632629"
---
# <a name="installercomponentpath-property"></a>Installer.ComponentPath, propiedad

La **propiedad ComponentPath** es una propiedad de solo lectura que devuelve la ruta de acceso completa a un componente instalado. Si la ruta de acceso de clave del componente es una clave del Registro, se devuelve la clave del Registro.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Si el componente es una clave del Registro, las raíces del Registro se representan numéricamente. Por ejemplo, una ruta de acceso del Registro de "HKEY CURRENT USER SOFTWARE Microsoft" se \_ \_ \\ \\ devolvería como "01: \\ SOFTWARE \\ Microsoft". Las raíces del registro devueltas se definen de la siguiente manera:



| Root                    | Valor devuelto |
|-------------------------|----------------|
| RAÍZ DE CLASES HKEY \_ \_     | 00             |
| USUARIO ACTUAL DE HKEY \_ \_     | 01             |
| HKEY \_ LOCAL \_ MACHINE    | 02             |
| USUARIOS DE \_ HKEY             | 03             |
| DATOS DE RENDIMIENTO DE HKEY \_ \_ | 04             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




