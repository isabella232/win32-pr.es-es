---
title: Propiedad AxWindowsMediaPlayer.cdromCollection
description: La propiedad cdromCollection obtiene una interfaz IWMPCdromCollection que proporciona acceso a una colección de unidades de CD o DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- CdromCollection, propiedad Reproductor de Windows Media
- Propiedad cdromCollection Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889793"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>Propiedad AxWindowsMediaPlayer.cdromCollection

La propiedad cdromCollection obtiene una **interfaz IWMPCdromCollection** que proporciona acceso a una colección de unidades de CD o DVD.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Valor de propiedad

Interfaz WMPLib.IWMPCdromCollection.

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





