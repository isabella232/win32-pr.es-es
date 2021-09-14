---
description: El método SourceListClearSource quita un origen de red o dirección URL. Acepta Type, el tipo de origen y SourcePath, la ruta de acceso de origen, como parámetros que se quitarán. Este método llama a MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Método Product.SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069780"
---
# <a name="productsourcelistclearsource-method"></a>Método Product.SourceListClearSource

El **método SourceListClearSource** quita un origen de red o dirección URL. Acepta *Type*, el tipo de origen y *SourcePath*, la ruta de acceso de origen, como parámetros que se quitarán. Este método llama a [**MsiSourceListClearSource.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de origen que se va a quitar: MSISOURCETYPE \_ NETWORK o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Ruta de acceso al origen que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




