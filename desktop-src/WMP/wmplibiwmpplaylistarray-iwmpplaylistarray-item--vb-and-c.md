---
title: Método IWMPPlaylistArray Item
description: El método Item devuelve una interfaz IWMPPlaylist que representa la lista de reproducción en el índice especificado.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Método de elemento Reproductor de Windows Media
- Método item Reproductor de Windows Media , interfaz IWMPPlaylistArray
- Interfaz IWMPPlaylistArray Reproductor de Windows Media , Método Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331164"
---
# <a name="iwmpplaylistarrayitem-method"></a>IWMPPlaylistArray::Item (Método)

El **método Item** devuelve una interfaz **IWMPPlaylist** que representa la lista de reproducción en el índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ En\]
</dt> <dd>

**System.Int32 que** contiene el índice que identifica la lista de reproducción que el método debe recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción recuperada.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





