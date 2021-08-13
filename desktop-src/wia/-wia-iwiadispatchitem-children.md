---
description: La propiedad Children del objeto Item recupera una colección de objetos Item. Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico. Solo lectura.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Propiedad Item.Children
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 72ce5119a10adc6a902d5a675d3ec116a3db1852a88e47ed852284cf44edf2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440734"
---
# <a name="itemchildren-property"></a>Propiedad Item.Children

La **propiedad Children** del objeto [**Item**](-wia-item.md) recupera una colección de **objetos Item.** Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico. Solo lectura.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Valor de propiedad

Variable que recibe los objetos .

## <a name="remarks"></a>Observaciones

Use esta propiedad para navegar por el árbol jerárquico de [**objetos Item**](-wia-item.md) que representan un dispositivo, las carpetas y los archivos que residen en el dispositivo.

La **propiedad Children** es una colección de objetos [**Item**](-wia-item.md) solo del nivel directamente debajo de este objeto **Item** en el árbol. Para navegar por los niveles lejos del árbol, use esta propiedad de forma recursiva.

Si el elemento no puede o no tiene ningún elemento secundario, esta propiedad devuelve una colección vacía.

> [!Note]  
> Esta colección está basada en 0.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **propiedad Children** para recuperar y enumerar una colección de los elementos secundarios de un dispositivo. Si el dispositivo es una cámara digital, la colección normalmente contiene elementos de carpeta e imagen. Si el dispositivo es un escáner, la colección normalmente contiene elementos que representan el examen.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




