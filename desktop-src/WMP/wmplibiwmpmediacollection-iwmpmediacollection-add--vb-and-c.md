---
title: Método add de IWMPMediaCollection
description: El método add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | Método add de IWMPMediaCollection
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- agregar método Reproductor de Windows Media
- add method Reproductor de Windows Media , IWMPMediaCollection (interfaz)
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861174"
---
# <a name="iwmpmediacollectionadd-method"></a>IWMPMediaCollection::add (método)

El **método add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* \[ En\]
</dt> <dd>

**System.String que** es la dirección URL que especifica la ubicación del elemento multimedia o la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPMedia** para el elemento o lista de reproducción agregados.

## <a name="remarks"></a>Comentarios

Este método carga un elemento multimedia o una lista de reproducción existentes en la biblioteca, dada una ruta de acceso. Este método no mueve ni cambia el archivo. Este método produce un error si se le da una ruta de acceso local no válida, pero no se comprueba la validez de los propios elementos multimedia antes de agregarlos a la biblioteca.

Este método acepta archivos de lista de reproducción estáticos y automáticos. El **método IWMPPlaylistCollection.importPlaylist** también se puede usar para agregar una lista de reproducción estática a la biblioteca.

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se agregan tres objetos multimedia a la colección Reproductor de Windows Media multimedia. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.remove (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.importPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





