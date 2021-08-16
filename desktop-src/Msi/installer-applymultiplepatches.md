---
description: El método ApplyMultiplePatches aplica una o varias revisiones a los productos que son aptos para recibir la revisión. El método establece la propiedad PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Método Installer.ApplyMultiplePatches
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
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633212"
---
# <a name="installerapplymultiplepatches-method"></a>Método Installer.ApplyMultiplePatches

El **método ApplyMultiplePatches** aplica una o varias revisiones a los productos que son aptos para recibir la revisión. El método establece la [**propiedad PATCH.**](patch.md)

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

Cadena que contiene una lista delimitada por punto y coma de las rutas de acceso a los archivos de revisión. Por ejemplo: ""c: \\ sus download cache Office \\ \\ \\ \\ sp1.msp; c: \\ sus download cache Office \\ \\ \\ \\ QFE1.msp;c: \\ sus download cache Office \\ \\ \\ \\ PEMEn.msp""

</dd> <dt>

*Producto* 
</dt> <dd>

Este parámetro proporciona el [**ProductCode**](productcode.md) del producto al que se va a aplicar la revisión. Este parámetro es opcional. Cuando este parámetro es NULL, las revisiones se aplican a todos los productos que son aptos para recibir estas revisiones.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Cadena terminada en NULL que especifica la configuración de propiedades de la línea de comandos. Este parámetro es opcional. Vea [Acerca de las propiedades](about-properties.md) y establecimiento de valores de propiedad pública en la línea de [comandos](setting-public-property-values-on-the-command-line.md). Todas las propiedades comparten todos los productos de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**Parche**](patch.md)
</dt> <dt>

[Establecer valores de propiedad pública en la línea de comandos](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




