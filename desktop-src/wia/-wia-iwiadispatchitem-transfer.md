---
description: El método Transfer del objeto Item transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Método Item.Transfer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: efef054a324244553748b75659820f582100a01ed6f56f9a2f80b0ef0c08f105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706325"
---
# <a name="itemtransfer-method"></a>Método Item.Transfer

El **método Transfer** del objeto [**Item**](-wia-item.md) transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo al que se transfieren los datos.

</dd> <dt>

*AsyncTransfer* \[ En\]
</dt> <dd>

Tipo: **VARIANT \_ BOOL**

Valor booleano que especifica si la transferencia debe ejecutarse como una llamada asincrónica.

<dt>



 (VARIANT \_ BOOL)


</dt> <dd>

Predeterminada. Establezca este valor en **true si** la llamada debe ser asincrónica (vea **Comentarios**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método solo se aplica a los elementos de tipo de archivo. El método comprueba que el elemento admite este método antes de intentar completar la transferencia de datos.

Use "portapapeles" como parámetro *Filename* para transferir un elemento al Portapapeles.

Establezca el valor *de AsyncTransfer* en **false** para las transferencias dentro de cualquier aplicación o script que se ejecute en un entorno que finalice un proceso al final de un script, como Windows Script Host (WSH). De lo contrario, el script puede finalizar y finalizar el proceso antes de que se complete la transferencia.

El **método Transfer** no tiene ningún valor devuelto. Tras la finalización de una transferencia, este método envía un [**evento OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) al script o a la aplicación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método Transfer** para transferir datos desde un dispositivo.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




