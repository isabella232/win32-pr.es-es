---
description: El método SourceListClearMediaDisk del objeto Product quita un disco especificado del conjunto de discos registrados para un producto. Acepta Diskid como parámetro. Este método llama a MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Método Product.SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069781"
---
# <a name="productsourcelistclearmediadisk-method"></a>Método Product.SourceListClearMediaDisk

El **método SourceListClearMediaDisk** del [**objeto Product**](product-object.md) quita un disco especificado del conjunto de discos registrados para un producto. Acepta *Diskid como* parámetro. Este método llama a [**MsiSourceListClearMediaDisk.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Diskid* 
</dt> <dd>

Este parámetro proporciona el identificador del disco que se va a quitar.

</dd> </dl>

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

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




