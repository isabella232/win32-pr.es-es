---
description: El método InstallProduct del objeto Installer abre un paquete del instalador e inicializa una sesión de instalación.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Instalador. InstallProduct (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653328"
---
# <a name="installerinstallproduct-method"></a>Instalador. InstallProduct (método)

El método **InstallProduct** del objeto [**Installer**](installer-object.md) abre un paquete del instalador e inicializa una sesión de instalación.

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

Cadena requerida que contiene la ruta de acceso al paquete de instalación.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Cadena opcional que contiene pares propiedad = valor separados por espacios en blanco.

Para realizar una instalación administrativa, incluya ACTION = ADMIN en *propertyValues*. Para obtener más información, vea la propiedad [**acción**](action.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para quitar completamente un producto, establezca REMOVE = ALL en *propertyValues*. Para obtener más información, vea [**Remove**](remove.md) Property.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




