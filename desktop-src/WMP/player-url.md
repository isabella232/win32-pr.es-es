---
title: Player. URL
description: La propiedad URL especifica o recupera el nombre del elemento multimedia que se va a reproducir.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Reproductor. URL de Windows Media Player
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
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708760"
---
# <a name="playerurl"></a>Player. URL

La propiedad **URL** especifica o recupera el nombre del elemento multimedia que se va a reproducir.

## <a name="syntax"></a>Sintaxis

*reproductor* . **Dirección URL**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura sin ningún valor predeterminado.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o la página web que realiza la llamada.

Las aplicaciones que abren elementos multimedia de detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.

No llame a este método desde el código del controlador de eventos. Llamando al *reproductor*. La **dirección URL** de un controlador de eventos puede producir resultados inesperados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de entrada de texto HTML y un elemento de entrada de botón HTML. El elemento de texto permite al usuario escribir una ruta de acceso para especificar un archivo multimedia digital que se va a reproducir. El elemento BUTTON ejecuta JScript que abre el archivo e inicia Windows Media Player. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





