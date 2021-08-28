---
description: La propiedad State devuelve el estado de instalación de esta instancia del producto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product.State, propiedad
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
ms.openlocfilehash: befa632feae7b4c57983f13a28e695051842cb5d1a2ff0908e6ffd011c6e4918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753955"
---
# <a name="productstate-property"></a>Product.State, propiedad

La **propiedad State** devuelve el estado de instalación de esta instancia del producto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.State
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve uno de los valores siguientes.



| Estado de instalación       | Significado                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE \_ DEFAULT    | Instancia del producto instalado localmente. |
| INSTALLSTATE \_ ANUNCIADO | Instancia del producto anunciado.        |
| INSTALLSTATE \_ UNKNOWN    | Instancia del producto desconocido.           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




