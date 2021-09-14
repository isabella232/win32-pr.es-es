---
description: El método InstallProduct del objeto Installer abre un paquete del instalador e inicializa una sesión de instalación.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer.InstallProduct (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072141"
---
# <a name="installerinstallproduct-method"></a>Installer.InstallProduct (método)

El **método InstallProduct** del objeto [**Installer**](installer-object.md) abre un paquete del instalador e inicializa una sesión de instalación.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Cadena necesaria que contiene la ruta de acceso al paquete de instalación.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Cadena opcional que contiene pares property=value separados por espacios en blanco.

Para realizar una instalación administrativa, incluya ACTION=ADMIN en *propertyValues*. Para obtener más información, vea la [**propiedad ACTION.**](action.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para quitar completamente un producto, establezca REMOVE=ALL en *propertyValues*. Para obtener más información, vea [**REMOVE property.**](remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




