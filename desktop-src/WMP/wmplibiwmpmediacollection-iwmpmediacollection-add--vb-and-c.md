---
title: IWMPMediaCollection Add (método)
description: El método Add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | IWMPMediaCollection Add (método)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Agregar método Media Player de Windows
- Agregar método Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método Add
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
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670362"
---
# <a name="iwmpmediacollectionadd-method"></a>IWMPMediaCollection:: Add (método)

El método **Add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.

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

*bstrURL* \[ de\]
</dt> <dd>

**System. String** que es la dirección URL que especifica la ubicación del elemento multimedia o de la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La interfaz **WMPLib. IWMPMedia** para el elemento o la lista de reproducción agregados.

## <a name="remarks"></a>Observaciones

Este método carga un elemento multimedia o una lista de reproducción existente en la biblioteca, dada una ruta de acceso. Este método no mueve ni cambia el archivo. Este método produce un error si se proporciona una ruta de acceso local no válida, pero no se comprueba la validez de los elementos multimedia en sí antes de que se agreguen a la biblioteca.

Este método acepta archivos de lista de reproducción estática y automática. También se puede usar el método **IWMPPlaylistCollection. importPlaylist** para agregar una lista de reproducción estática a la biblioteca.

Antes de llamar a este método, debe tener acceso total a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se agregan tres objetos multimedia a la colección de medios de Windows Media Player. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


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
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. Remove (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





