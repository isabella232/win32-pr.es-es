---
description: El método transfer del objeto Item transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer (método)
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
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696617"
---
# <a name="itemtransfer-method"></a>Item. Transfer (método)

El método **Transfer** del objeto [**Item**](-wia-item.md) transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo al que se transfieren los datos.

</dd> <dt>

*AsyncTransfer* \[ de\]
</dt> <dd>

Tipo: **variante \_ bool**

Valor booleano que especifica si la transferencia se debe ejecutar como una llamada asincrónica.

<dt>



 (Variante \_ BOOLEANO


</dt> <dd>

Predeterminada. Establezca este valor en **true** si la llamada debe ser asincrónica (vea la **sección Comentarios**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método solo se aplica a los elementos de tipo de archivo. El método comprueba que el elemento admite este método antes de intentar completar la transferencia de datos.

Use "Clipboard" como parámetro *filename* para transferir un elemento al portapapeles.

Establezca el valor de *AsyncTransfer* en **false** para las transferencias de cualquier aplicación o script que se ejecute en un entorno que termine un proceso al final de un script, como Windows Script Host (WSH). De lo contrario, el script puede finalizar y el proceso finaliza antes de que se complete la transferencia.

El método **Transfer** no tiene ningún valor devuelto. Tras la finalización de una transferencia, este método envía un evento [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) al script o la aplicación.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso del método **Transfer** para transferir datos desde un dispositivo.


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




