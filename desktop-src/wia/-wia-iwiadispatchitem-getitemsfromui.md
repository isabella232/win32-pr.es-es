---
description: El método GetItemsFromUI del objeto Item muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI (método)
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
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154865"
---
# <a name="itemgetitemsfromui-method"></a>Item. GetItemsFromUI (método)

El método **GetItemsFromUI** del objeto [**Item**](-wia-item.md) muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Predeterminada. \[en \] especifica el comportamiento del cuadro de diálogo. Los valores válidos para este parámetro son los mismos que para el parámetro *lFlags* del método [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .

</dd> </dl> </dd> <dt>

*Intención* \[ de\]
</dt> <dd>

Tipo: **WiaIntent**

<dt>



  (0)


</dt> <dd>

Predeterminada. \[en \] especifica qué tipo de datos pretende representar la imagen. Para obtener una lista de valores de intención de imagen, vea [**constantes de intención de imagen**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **ICollection**

Este método devuelve una colección de objetos de [**elemento**](-wia-item.md) que representan los elementos seleccionados por el usuario. Si no se selecciona ningún elemento, la colección está vacía.

## <a name="remarks"></a>Observaciones

En el caso de las aplicaciones de Microsoft Visual Basic, agregue una referencia a "biblioteca de tipos 1,01 de adquisición de imágenes de Windows".

Este método solo se aplica a los dispositivos (elementos raíz). El método devuelve una colección de objetos de [**elemento**](-wia-item.md) que representan las imágenes o los clips de audio seleccionados por el usuario.

Si el usuario no selecciona ningún elemento, el método devuelve una colección vacía.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del método **GetItemsFromUI** para permitir que un usuario seleccione imágenes en un cuadro de diálogo.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




