---
description: El método GetItemsFromUI del objeto Item muestra un cuadro de diálogo que permite a un usuario seleccionar imágenes y audio para transferir desde un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Método Item.GetItemsFromUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669717"
---
# <a name="itemgetitemsfromui-method"></a>Método Item.GetItemsFromUI

El **método GetItemsFromUI** del objeto [**Item**](-wia-item.md) muestra un cuadro de diálogo que permite a un usuario seleccionar imágenes y audio para transferir desde un dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Predeterminada. \[en \] Especifica el comportamiento del cuadro de diálogo. Los valores válidos para este parámetro son los mismos que para el *parámetro lFlags* del [**método DeviceDlg.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)

</dd> </dl> </dd> <dt>

*Intención* \[ En\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  (0)


</dt> <dd>

Predeterminada. \[en \] Especifica el tipo de datos que la imagen pretende representar. Para obtener una lista de valores de intención de imagen, vea [**Constantes de intención de imagen.**](-wia-imageintentconstants.md)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **ICollection**

Este método devuelve una colección de [**objetos Item**](-wia-item.md) que representan los elementos seleccionados por el usuario. Si no se selecciona ningún elemento, la colección está vacía.

## <a name="remarks"></a>Comentarios

Para las aplicaciones Visual Basic Microsoft, agregue una referencia a "Windows biblioteca de tipos de adquisición de imágenes 1.01".

Este método solo se aplica a dispositivos (elementos raíz). El método devuelve una colección de objetos [**Item**](-wia-item.md) que representan las imágenes o clips de audio seleccionados por el usuario.

Si el usuario no selecciona ningún elemento, el método devuelve una colección vacía.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método GetItemsFromUI** para permitir que un usuario seleccione imágenes de un cuadro de diálogo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




