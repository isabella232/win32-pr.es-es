---
title: IWMPCdromRip startRip, método
description: El método startRip RIP el CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- método startRip de Windows Media Player
- método startRip Windows Media Player, interfaz IWMPCdromRip
- Interfaz IWMPCdromRip Windows Media Player, método startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649912"
---
# <a name="iwmpcdromripstartrip-method"></a>IWMPCdromRip:: startRip (método)

El método **startRip** RIP el CD.

## <a name="syntax"></a>Sintaxis


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La copia desde CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player. El contenido copiado se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información acerca de las preferencias de usuario para la copia desde CD, consulte "copiar música desde CDs" en la ayuda de Windows Media Player.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRip (VB y C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**IWMPCdromRip.stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[**Copia desde CD**](ripping-a-cd.md)
</dt> </dl>

 

 





