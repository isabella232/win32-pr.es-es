---
description: La propiedad Sources enumera todos los orígenes de la instancia de producto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Propiedad Product.Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069773"
---
# <a name="productsources-property"></a>Propiedad Product.Sources

La **propiedad Sources** enumera todos los orígenes de la instancia de producto. Esta propiedad llama [**a MsiSourceListEnumSources,**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) devuelve la matriz de cadenas y acepta el tipo de origen como argumento. El tipo de origen puede ser MSISOURCETYPE \_ NETWORK o MSISOURCETYPE \_ URL.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>Valor de propiedad

Tipo de origen que se enumerará. El valor puede ser *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-00000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




