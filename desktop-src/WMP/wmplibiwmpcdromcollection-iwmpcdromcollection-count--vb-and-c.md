---
title: Propiedad count de IWMPCdromCollection
description: La propiedad count obtiene el número de unidades de CD y DVD disponibles en el sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- count property Reproductor de Windows Media
- count property Reproductor de Windows Media , IWMPCdromCollection (interfaz)
- Interfaz IWMPCdromCollection Reproductor de Windows Media , propiedad count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569001"
---
# <a name="iwmpcdromcollectioncount-property"></a>Propiedad IWMPCdromCollection::count

La **propiedad count** obtiene el número de unidades de CD y DVD disponibles en el sistema.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el recuento de unidades disponibles.

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Las unidades de DVD se cuentan exactamente igual que las unidades de CD. Sin embargo, el control Reproductor de Windows Media ActiveX solo admite la funcionalidad de DVD Windows XP o posterior. Normalmente, las unidades de DVD pueden reproducir medios de CD, pero las unidades de CD no pueden reproducir medios de DVD.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa count para mostrar el número de unidades de CD y DVD disponibles en un cuadro de mensaje. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





