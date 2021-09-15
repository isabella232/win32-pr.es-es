---
title: Propiedad IWMPCdromRomRom burnPlaylist
description: La propiedad burnPlaylist obtiene la lista de reproducción actual para grabar en el CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- propiedades burnPlaylist Reproductor de Windows Media
- Interfaz de propiedad burnPlaylist Reproductor de Windows Media , IWMPCdromRomRom
- Interfaz IWMPCdromRom Reproductor de Windows Media , propiedad burnPlaylist
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569040"
---
# <a name="iwmpcdromburnburnplaylist-property"></a>Propiedad IWMPCdromRomRom::burnPlaylist

La **propiedad burnPlaylist** obtiene la lista de reproducción actual para grabar en el CD.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a>Valor de propiedad

Interfaz **WMPLib.IWMPPlaylist** de la lista de reproducción que se grabará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11<br/>                                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromRom (VB y C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





