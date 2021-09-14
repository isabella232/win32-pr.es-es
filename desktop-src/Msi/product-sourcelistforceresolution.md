---
description: El método SourceListForceResolution borra la propiedad LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Método Product.SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069779"
---
# <a name="productsourcelistforceresolution-method"></a>Método Product.SourceListForceResolution

El **método SourceListForceResolution** borra la propiedad LastUsedSource. Esto obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se requiera un origen, como cuando el instalador realiza una instalación o una reinstalación, o cuando se requiere la ruta de acceso para que un conjunto de componentes se ejecute desde el origen.

Este método llama a [**MsiSourceListForceResolution.**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




