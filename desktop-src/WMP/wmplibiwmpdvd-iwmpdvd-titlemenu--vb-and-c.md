---
title: IWMPDVD titleMenu, método
description: El método titleMenu detiene la reproducción y muestra el menú de título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- método titleMenu de Windows Media Player
- método titleMenu Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661219"
---
# <a name="iwmpdvdtitlemenu-method"></a>IWMPDVD:: titleMenu (método)

El método **titleMenu** detiene la reproducción y muestra el menú de título.

## <a name="syntax"></a>Sintaxis


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVDs se crean para que los métodos **IWMPDVD.** **titleMenu y** abran el mismo menú. El método **titleMenu** normalmente invoca el menú de título, pero puede invocar el menú superior si no hay ningún menú de título disponible.

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

[**IWMPDVD. webmenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





