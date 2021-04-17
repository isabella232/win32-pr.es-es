---
description: El método OpenPackage del objeto Installer abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto e instalan el motor, y devuelven un objeto de sesión.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Instalador. OpenPackage (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653323"
---
# <a name="installeropenpackage-method"></a>Instalador. OpenPackage (método)

El método **OpenPackage** del objeto [**Installer**](installer-object.md) abre un paquete del instalador para su uso con funciones que tienen acceso a la base de datos del producto e instalan el motor, y devuelven un objeto de [**sesión**](session-object.md) .

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

Cadena requerida que contiene el nombre de la ruta de acceso del paquete.

</dd> <dt>

*options* 
</dt> <dd>

Valor entero opcional que especifica si **OpenPackage** debe omitir el estado actual del equipo al crear el objeto de sesión. Ningún valor o un valor de 0 para Options tiene como valor predeterminado el comportamiento original. Cuando Options es 1, el método **OpenPackage** omite el estado actual del equipo al abrir el paquete. Un valor de 1 impide que se realicen cambios en el estado actual del equipo. Para obtener más información, vea [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **OpenPackage** puede aceptar el identificador de la base de datos directamente en lugar de la cadena de la ruta de acceso del paquete.

Tenga en cuenta que solo un único proceso puede abrir un objeto de [**sesión**](session-object.md) . **OpenPackage** no se puede usar en una acción personalizada porque la instalación activa es la única sesión permitida.

Un objeto de [**sesión**](session-object.md) segura omite el estado actual del equipo al abrir el paquete y evita los cambios en el estado actual del equipo. Para obtener más información, vea [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




