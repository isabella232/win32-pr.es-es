---
title: Propiedad IWMPCdrom driveSpecifier
description: La propiedad driveSpecifier obtiene la letra de unidad de CD o DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- Propiedad driveSpecifier Reproductor de Windows Media
- Propiedad driveSpecifier Reproductor de Windows Media , interfaz IWMPCdrom
- Interfaz IWMPCdrom Reproductor de Windows Media , propiedad driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374266"
---
# <a name="iwmpcdromdrivespecifier-property"></a>IWMPCdrom::d riveSpecifier

La **propiedad driveSpecifier** obtiene la letra de unidad de CD o DVD.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es la letra de unidad.

## <a name="remarks"></a>Observaciones

Normalmente, las unidades de DVD pueden reproducir medios de CD, pero las unidades de CD no pueden reproducir medios de DVD.

Esta propiedad obtiene una letra de unidad para un índice de unidad de base cero dentro del intervalo recuperado mediante **IWMPCdromCollection.count**. El valor recuperado tiene la forma *X*:, donde *X* representa la letra de unidad.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa driveSpecifier** para compilar una cadena que contiene una lista de unidades de CD y DVD disponibles y muestra esa cadena en un cuadro de mensaje. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdromCollection.count (VB y C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





