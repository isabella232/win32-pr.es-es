---
description: La propiedad ProductState es una propiedad de solo lectura que devuelve la información de estado de instalación de un producto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Instalador. ProductState (método de propiedad)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653713"
---
# <a name="installerproductstate-property-method"></a>Instalador. ProductState (método de propiedad)

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
| msiInstallStateAbsent     | El producto se instala para un usuario diferente.   |
| msiInstallStateDefault    | El producto está instalado para el usuario actual.   |
| msiInstallStateAdvertised | El producto se anuncia pero no se instala.     |
| msiInstallStateInvalidArg | Se pasó un parámetro no válido a la función. |
| msiInstallStateUnknown    | El producto no se anuncia ni se instala. |
| msiInstallStateBadConfig  | Los datos de configuración están dañados.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




