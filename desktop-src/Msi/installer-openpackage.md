---
description: El método OpenPackage del objeto Installer abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto y al motor de instalación, devolviendo un objeto Session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer.OpenPackage (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072133"
---
# <a name="installeropenpackage-method"></a>Installer.OpenPackage (método)

El **método OpenPackage** del objeto [**Installer**](installer-object.md) abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto y al motor de instalación, devolviendo un [**objeto Session.**](session-object.md)

## <a name="syntax"></a>Sintaxis


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Cadena necesaria que contiene el nombre de ruta de acceso del paquete.

</dd> <dt>

*options* 
</dt> <dd>

Valor entero opcional que especifica si **OpenPackage** debe omitir o no el estado actual del equipo al crear el objeto Session. Ningún valor o un valor de 0 para las opciones tiene como valor predeterminado el comportamiento original. Cuando options es 1, el **método OpenPackage** omite el estado actual del equipo al abrir el paquete. Un valor de 1 impide los cambios en el estado actual del equipo. Para obtener más información, [**vea MsiOpenPackageEx.**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método OpenPackage** puede aceptar el identificador de base de datos directamente en lugar de la cadena para la ruta de acceso del paquete.

Tenga en cuenta que solo un [**proceso**](session-object.md) puede abrir un objeto Session. **OpenPackage** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.

Un objeto [**Session**](session-object.md) seguro omite el estado actual del equipo al abrir el paquete e impide los cambios en el estado actual del equipo. Para obtener más información, [**vea MsiOpenPackageEx.**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




