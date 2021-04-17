---
description: El método ApplyMultiplePatches aplica una o más revisiones a los productos que son válidos para recibir la revisión. El método establece la propiedad PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Instalador. ApplyMultiplePatches (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653641"
---
# <a name="installerapplymultiplepatches-method"></a>Instalador. ApplyMultiplePatches (método)

El método **ApplyMultiplePatches** aplica una o más revisiones a los productos que son válidos para recibir la revisión. El método establece la propiedad [**patch**](patch.md) .

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

Una cadena que contiene una lista delimitada por signos de punto y coma de las rutas de acceso a los archivos de revisión. Por ejemplo: "c: \\ sus \\ Descargar \\ caché \\ Office \\ SP1. MSP; c: \\ \\ descargar el \\ almacenamiento en caché de \\ Office \\ QFE1. MSP; c: \\ sus \\ Descargar \\ caché \\ Office \\ QFEn. MSP ""

</dd> <dt>

*Producto* 
</dt> <dd>

Este parámetro proporciona el [**ProductCode**](productcode.md) del producto que se va a revisar. Este parámetro es opcional. Cuando este parámetro es null, las revisiones se aplican a todos los productos que son válidos para recibir estas revisiones.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Una cadena terminada en null que especifica los valores de propiedades de la línea de comandos. Este parámetro es opcional. Vea [acerca de las propiedades](about-properties.md) y [establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md). Todas las propiedades son compartidas por todos los productos de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**DISTRIBUCIÓN**](patch.md)
</dt> <dt>

[Establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




