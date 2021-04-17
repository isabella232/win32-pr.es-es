---
description: El método RemovePatches quita una o más revisiones de los productos que puedan recibir la revisión. El método RemovePatches llama a MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Instalador. RemovePatches (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653708"
---
# <a name="installerremovepatches-method"></a>Instalador. RemovePatches (método)

El método **RemovePatches** quita una o más revisiones de los productos que puedan recibir la revisión. El método **RemovePatches** llama a [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

## <a name="syntax"></a>Sintaxis


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PatchList* 
</dt> <dd>

Una cadena que contiene una lista delimitada por punto y coma de las revisiones que se van a quitar. Cada revisión se puede representar mediante la ruta de acceso completa al paquete de revisión o mediante el GUID de la revisión. Este parámetro es necesario.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Cadena con el GUID del producto del que se van a quitar las revisiones. Este parámetro es necesario.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Valor entero que especifica el tipo de eliminación de la revisión. Este parámetro debe ser **msiInstallTypeSingleInstance**.

</dd> <dt>

*PropertyList* 
</dt> <dd>

Cadena que especifica los pares propiedad = valor que se van a incluir. Este parámetro es opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Consulte [desinstalación de revisiones](uninstalling-patches.md) para obtener un ejemplo que muestra cómo una aplicación puede quitar una revisión de todos los productos que están disponibles para el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




