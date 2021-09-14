---
title: Método back de IWMPDVD
description: El método back cambia la presentación de un submenú a su menú primario.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- back method Reproductor de Windows Media
- Método back Reproductor de Windows Media , interfaz IWMPDVD
- Interfaz IWMPDVD Reproductor de Windows Media , método back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242955"
---
# <a name="iwmpdvdback-method"></a>IWMPDVD::back (método)

El **método back** cambia la presentación de un submenú a su menú primario.

## <a name="syntax"></a>Sintaxis


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada DVD se ha escrito de forma diferente. Algunos DVD se crearon para que el método esté disponible en el menú raíz, pero cuando se invoque, `back` no hará nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





