---
title: Player.URL
description: La propiedad URL especifica o recupera el nombre del elemento multimedia que se reproducirá.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player.URL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00a6513350ee9c39855aba8168faf9ced788a0686a0fdbe845013dcc521142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572044"
---
# <a name="playerurl"></a>Player.URL

La **propiedad URL** especifica o recupera el nombre del elemento multimedia que se reproducirá.

## <a name="syntax"></a>Syntax

*player* . **Dirección URL**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de **lectura** y escritura sin ningún valor predeterminado.

## <a name="remarks"></a>Comentarios

Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o página web que realiza la llamada.

Las aplicaciones que abren elementos multimedia desde detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

No llame a este método desde el código del controlador de eventos. Llamar *al Reproductor* de . **La dirección URL** de un controlador de eventos puede producir resultados inesperados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de entrada HTML TEXT y un elemento de entrada HTML BUTTON. El elemento TEXT permite al usuario escribir una ruta de acceso para especificar un archivo multimedia digital que se reproducirá. El elemento BUTTON ejecuta JScript que abre el archivo e inicia Reproductor de Windows Media. El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





