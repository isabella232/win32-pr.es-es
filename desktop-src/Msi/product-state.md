---
description: La propiedad State devuelve el estado de instalación de esta instancia del producto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propiedad Product.State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069772"
---
# <a name="productstate-property"></a>Propiedad Product.State

La **propiedad State** devuelve el estado de instalación de esta instancia del producto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve uno de los valores siguientes.



| Estado de instalación       | Significado                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE \_ DEFAULT    | Instancia del producto instalado localmente. |
| INSTALLSTATE \_ ANUNCIADO | Instancia del producto anunciado.        |
| INSTALLSTATE \_ UNKNOWN    | Instancia del producto desconocido.           |



 

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

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




