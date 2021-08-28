---
title: Método titleMenu de IWMPDVD
description: El método titleMenu detiene la reproducción y muestra el menú de título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- método titleMenu Reproductor de Windows Media
- Método titleMenu Reproductor de Windows Media , interfaz IWMPDVD
- Interfaz IWMPDVD Reproductor de Windows Media método , titleMenu
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
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000465"
---
# <a name="iwmpdvdtitlemenu-method"></a>IWMPDVD::titleMenu (método)

El **método titleMenu** detiene la reproducción y muestra el menú de título.

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

## <a name="remarks"></a>Comentarios

Cada DVD se ha escrito de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVD se han escrito para que los métodos **IWMPDVD.topMenu** y **titleMenu** abran el mismo menú. El **método titleMenu** normalmente invoca el menú de título, pero puede invocar el menú superior si no hay ningún menú de título disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.topMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





