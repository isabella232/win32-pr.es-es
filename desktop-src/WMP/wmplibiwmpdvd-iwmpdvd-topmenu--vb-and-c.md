---
title: Método topMenu de IWMPDVD
description: El método topMenu detiene la reproducción y muestra el menú superior (o raíz) del título actual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Método topMenu Reproductor de Windows Media
- Método topMenu Reproductor de Windows Media , interfaz IWMPDVD
- Interfaz IWMPDVD Reproductor de Windows Media , método topMenu
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465716"
---
# <a name="iwmpdvdtopmenu-method"></a>IWMPDVD::topMenu (método)

El **método topMenu** detiene la reproducción y muestra el menú superior (o raíz) del título actual.

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

Cada DVD se ha escrito de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVD se han escrito para que los métodos **topMenu** e **IWMPDVD.titleMenu** abran el mismo menú. El **método topMenu** normalmente invoca el menú superior (o raíz), pero puede invocar el menú de título si no hay ningún menú raíz disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB y C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





