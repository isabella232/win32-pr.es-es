---
title: Evento Player.ScriptCommand
description: El evento ScriptCommand tiene lugar cuando se recibe un comando o una dirección URL sincronizados. | Evento Player.ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand event Reproductor de Windows Media
- ScriptCommand event Reproductor de Windows Media , Player (Clase)
- Clase player Reproductor de Windows Media , evento ScriptCommand
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068357"
---
# <a name="playerscriptcommand-event"></a>Evento Player.ScriptCommand

El **evento ScriptCommand** tiene lugar cuando se recibe un comando o una dirección URL sincronizados.

## <a name="syntax"></a>Sintaxis


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*scType* 
</dt> <dd>

Cadena que especifica el tipo de comando de script.

</dd> <dt>

*Param* 
</dt> <dd>

**Cadena** que especifica el comando de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los comandos se pueden incrustar entre los sonidos e imágenes de un Windows o secuencia multimedia. Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia. Cuando la secuencia alcanza el tiempo asociado al comando, el control Reproductor de Windows Media envía un **evento ScriptCommand** con dos parámetros. Un parámetro especifica el tipo de comando que se envía y el otro parámetro especifica el comando . El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando. Cualquier tipo de comando se puede incrustar en un archivo o secuencia para que lo controle el **evento ScriptCommand.**

En la tabla siguiente se enumeran los tipos de comandos de script que los Reproductor de Windows Media.



| Tipo                   | Descripción                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.                                                                  |
| EVENTO                  | Indica al control que ejecute las instrucciones definidas para el evento especificado.                                                                                          |
| NOMBRE               | El control restablece su propiedad **URL,** intenta abrir el archivo especificado y comienza a reproducir la nueva secuencia inmediatamente.                                        |
| OPENEVENT              | Almacena en búfer el comando event type asociado para la ejecución a tiempo del script EVENT.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | El *parámetro Param* contiene el texto sincronizado. Reproductor de Windows Media muestra el texto del cuadro de texto en el área de título cerrada de la **característica Reproducción** ahora. |
| TEXT                   | El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.                                                                  |
| URL                    | El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado si el *Configuración*. **La propiedad invokeURLs** se establece en true.                      |



 

Puede insertar cualquier otro tipo de comando siempre que proporcione código recíproco para controlar el comando. Aunque el control Reproductor de Windows Media los comandos desconocidos, se siguen entregando al **evento ScriptCommand.**

Los comandos de dirección URL recibidos por Reproductor de Windows Media control se invocan automáticamente en el explorador web predeterminado si el *Configuración*. **La propiedad invokeURLs** se establece en true. Puede usar el *Configuración*. **propiedad defaultFrame** para especificar el marco de destino en el que aparece la página web.

La dirección URL enviada a Reproductor de Windows Media se procesa con respecto a la dirección URL base especificada por *el Configuración*. **propiedad baseURL.** La dirección URL base se concatena con la dirección URL relativamente especificada, lo que da lugar a una dirección URL totalmente especificada que el evento **ScriptCommand** pasa como parámetro de comando.

El Reproductor de Windows Media control siempre procesa los comandos entrantes de tipo URL de la siguiente manera:

1.  Se recibe un comando de tipo URL.
2.  *Configuración*. **baseURL** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.
3.  Se llama a *ScriptCommand.*
4.  Cuando *scriptCommand* vuelva, *Configuración*. **InvokeURLs** está activado.
5.  Si *Configuración*. **invokeURLs** es true y el comando es un tipo de dirección URL, se invoca la dirección URL especificada. Si *Configuración*. **invokeURLs** es false o si el comando no es un tipo de dirección URL, se omite el comando.

Al crear un archivo multimedia Windows, puede especificar en qué marco se muestra la nueva dirección URL mediante la concatenación de dos y comercial y el nombre del marco en el campo de parámetro. En el ejemplo siguiente se muestran los parámetros *scriptCommand* típicos. Especifica que la dirección URL *mypage* debe iniciarse en el *marco myframe.*


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



No se llama al evento ScriptCommand si se está analizando el archivo (reenviado rápido o invertido rápidamente).

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> <dt>

[**Configuración.baseURL**](settings-baseurl.md)
</dt> <dt>

[**Configuración.defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Configuración.invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





