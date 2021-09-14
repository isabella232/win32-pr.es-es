---
description: La propiedad ProductState es una propiedad de solo lectura que devuelve la información de estado de instalación de un producto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Método Installer.ProductState Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072111"
---
# <a name="installerproductstate-property-method"></a>Método Installer.ProductState Property

La **propiedad ProductState** es una propiedad de solo lectura que devuelve la información de estado de instalación de un producto.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código de producto del producto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Devuelve uno de los valores que se muestran en la tabla siguiente.



| Estado de instalación        | Descripción                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | El producto se instala para otro usuario.   |
| msiInstallStateDefault    | El producto se instala para el usuario actual.   |
| msiInstallStateAdvertised | El producto se anuncia pero no se instala.     |
| msiInstallStateInvalidArg | Se pasó un parámetro no válido a la función. |
| msiInstallStateUnknown    | El producto no se anuncia ni se instala. |
| msiInstallStateBadConfig  | Los datos de configuración están dañados.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




