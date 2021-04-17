---
description: La propiedad State devuelve el estado de instalación de esta instancia del producto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propiedad product. State
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653809"
---
# <a name="productstate-property"></a>Propiedad product. State

La propiedad **State** devuelve el estado de instalación de esta instancia del producto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve uno de los valores siguientes.



| Estado de la instalación       | Significado                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE ( \_ valor predeterminado)    | Instancia de producto instalada localmente. |
| INSTALLSTATE \_ anunciado | Instancia de producto anunciada.        |
| INSTALLSTATE \_ desconocido    | Instancia de producto desconocida.           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




