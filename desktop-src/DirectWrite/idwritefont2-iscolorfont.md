---
title: IDWriteFont2 IsColorFont, método
description: Permite determinar si es posible que una ruta de representación de color sea necesaria.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Método IsColorFont de escritura directa
- Método IsColorFont de escritura directa, interfaz IDWriteFont2
- Interfaz IDWriteFont2 Direct Write, método IsColorFont
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422445"
---
# <a name="idwritefont2iscolorfont-method"></a>IDWriteFont2:: IsColorFont (método)

Permite determinar si es posible que una ruta de representación de color sea necesaria.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve **true** si la fuente tiene información de color (tablas COLR y CPAL); en caso contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





