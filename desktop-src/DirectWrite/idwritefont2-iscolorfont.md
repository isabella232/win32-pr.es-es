---
title: Método IDWriteFont2 IsColorFont
description: Permite determinar si una ruta de acceso de representación de color es potencialmente necesaria.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Escritura directa del método IsColorFont
- Método IsColorFont direct write , interfaz IDWriteFont2
- Método Direct Write de la interfaz IDWriteFont2 , IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476936"
---
# <a name="idwritefont2iscolorfont-method"></a>Método IDWriteFont2::IsColorFont

Permite determinar si una ruta de acceso de representación de color es potencialmente necesaria.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Devuelve **TRUE** si la fuente tiene información de color (tablas COLR y CPAL); en caso **contrario, FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





