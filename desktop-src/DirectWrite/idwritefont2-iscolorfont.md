---
title: Método IDWriteFont2 IsColorFont
description: Permite determinar si una ruta de acceso de representación de color es potencialmente necesaria.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Escritura directa del método IsColorFont
- Método IsColorFont Direct Write , interfaz IDWriteFont2
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
ms.openlocfilehash: 144aded290c7a4121dd785a1844971e3c1b5501b8ae78707d8da5378c44b002a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650189"
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
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 y Windows runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





