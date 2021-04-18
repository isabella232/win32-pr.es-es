---
title: IWMPDVD (método de menú)
description: El método de menú de menús detiene la reproducción y muestra el menú superior (o raíz) del título actual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- método de menú de menús Media Player Windows
- método de menú de menús Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, método de menú de menús
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718973"
---
# <a name="iwmpdvdtopmenu-method"></a>IWMPDVD:: webmenu (método)

El método de **menú de menús** detiene la reproducción y muestra el menú superior (o raíz) del título actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVDs se crean para que los métodos de **menú** y **IWMPDVD. titleMenu** abran el mismo menú. El método de **menú de menús** suele invocar el menú superior (o raíz), pero puede invocar el menú de título si no hay ningún menú raíz disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





