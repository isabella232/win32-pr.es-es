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
ms.openlocfilehash: dec885de319153383b82359e35208d19031fa7378749b39033402aba11f8dbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055023"
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

## <a name="remarks"></a>Comentarios

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





