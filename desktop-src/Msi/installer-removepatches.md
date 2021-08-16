---
description: El método RemovePatches quita una o varias revisiones a los productos aptos para recibir la revisión. El método RemovePatches llama a MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer.RemovePatches (método)
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
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894035"
---
# <a name="installerremovepatches-method"></a>Installer.RemovePatches (método)

El **método RemovePatches** quita una o varias revisiones a los productos aptos para recibir la revisión. El **método RemovePatches** llama [**a MsiRemovePatches.**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)

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

Cadena que contiene una lista delimitada por punto y coma de revisiones que se deben quitar. Cada revisión se puede representar mediante la ruta de acceso completa al paquete de revisión o mediante el GUID de revisión. Este parámetro es obligatorio.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Cadena con el GUID del producto del que se van a quitar las revisiones. Este parámetro es obligatorio.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Valor entero que especifica el tipo de eliminación de revisiones. Este parámetro debe ser **msiInstallTypeSingleInstance.**

</dd> <dt>

*PropertyList* 
</dt> <dd>

Cadena que especifica los pares Property=Value que se incluirán. Este parámetro es opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Consulte [Desinstalar revisiones para obtener un](uninstalling-patches.md) ejemplo que muestra cómo una aplicación puede quitar una revisión de todos los productos que están disponibles para el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Desinstalación de revisiones](uninstalling-patches.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




