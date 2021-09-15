---
title: THEME.openDialog
description: El método openDialog abre un cuadro de diálogo de archivo.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEME.openDialog Reproductor de Windows Media
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258743"
---
# <a name="themeopendialog"></a>THEME.openDialog

El **método openDialog** abre un cuadro de diálogo de archivo.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

Cadena **que** especifica el tipo de cuadro de diálogo. Debe establecerse en "FILE \_ OPEN".

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*Parámetros*
</dt> <dd>

Cadena **que** se puede usar para obtener información adicional. Debe establecerse en "FILES \_ ALLMEDIA".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena que** contiene la dirección URL del archivo seleccionado o "" (cadena vacía) si el usuario hace clic en Cancelar.

## <a name="remarks"></a>Observaciones

Este método se puede usar para archivos en las unidades de disco duro locales o en unidades de red.

## <a name="examples"></a>Ejemplos


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO THEME**](theme-element.md)
</dt> </dl>

 

 





