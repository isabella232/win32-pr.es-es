---
title: Evento Player. comando
description: El evento comando se produce cuando se recibe un comando o una dirección URL sincronizados. | Evento Player. comando
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Media Player comando de eventos de Windows
- Evento comando de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento comando
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709274"
---
# <a name="playerscriptcommand-event"></a>Evento Player. comando

El evento **comando** se produce cuando se recibe un comando o una dirección URL sincronizados.

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

*Parámetro* 
</dt> <dd>

**Cadena** que especifica el comando de script.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los comandos se pueden insertar entre los sonidos e imágenes de un archivo o una secuencia de Windows Media. Los comandos son un par de cadenas Unicode asociadas a una hora designada en la secuencia. Cuando el flujo alcanza el tiempo asociado con el comando, el control Media Player de Windows envía un evento **comando** con dos parámetros. Un parámetro especifica el tipo de comando que se va a enviar y el otro parámetro especifica el comando. El tipo de parámetro se usa para determinar cómo se procesa el parámetro de comando. Cualquier tipo de comando se puede incrustar en un archivo o una secuencia para que lo controle el evento **comando** .

En la tabla siguiente se enumeran los tipos de comando de script que Windows Media Player procesa automáticamente.



| Tipo                   | Descripción                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.                                                                  |
| CESO                  | Indica al control que ejecute instrucciones definidas para el evento especificado.                                                                                          |
| EXTENSIÓN               | El control restablece su propiedad de **dirección URL** , intenta abrir el archivo especificado y comienza a reproducir el nuevo flujo inmediatamente.                                        |
| OPENEVENT              | Almacena en búfer el comando de tipo de evento asociado para la ejecución oportuna del script de eventos.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | El parámetro *param* contiene el texto de letra sincronizado. Windows Media Player muestra el texto de letra en el área de subtítulos (CC) de la característica de **reproducción en curso** . |
| TEXT                   | El control muestra el texto asociado en el DIV especificado por *ClosedCaption*. **captioningID**.                                                                  |
| URL                    | El control abre automáticamente la dirección URL especificada mediante el explorador de Internet predeterminado, si se trata de la *configuración*. la propiedad **invokeURLs** está establecida en true.                      |



 

Puede incrustar cualquier otro tipo de comando siempre que proporcione código recíproco para controlar el comando. Aunque el control de Windows Media Player omite los comandos desconocidos, se siguen entregando al evento **comando** .

Los comandos de dirección URL recibidos por el control Media Player de Windows se invocan automáticamente en el explorador Web predeterminado si se trata de la *configuración*. la propiedad **invokeURLs** está establecida en true. Puede usar la *configuración*. propiedad **defaultFrame** para especificar el marco de destino en el que aparece la Página Web.

La dirección URL enviada a Windows Media Player se procesa con respecto a la dirección URL base especificada en la *configuración*. propiedad **baseurl** . La dirección URL base se concatena con la dirección URL relativamente especificada, lo que da como resultado una dirección URL totalmente especificada que se pasa como parámetro de comando por el evento **comando** .

El control Windows Media Player siempre procesa los comandos de tipo URL de entrada de la siguiente manera:

1.  Se recibe un comando de tipo URL.
2.  *Configuración*. **baseurl** se usa para crear una dirección URL completa a partir de la dirección URL relativa especificada en el comando de script.
3.  Se llama a *comando* .
4.  Después de que *comando* devuelve, *configuración*. **invokeURLs** está activada.
5.  Es si se trata de un *valor*. **invokeURLs** es true y el comando es un tipo de dirección URL; se invoca la dirección URL especificada. Es si se trata de un *valor*. **invokeURLs** es false o si el comando no es un tipo de dirección URL, se omite el comando.

Al crear un archivo de Windows Media, puede especificar el marco en el que se muestra la nueva dirección URL mediante la concatenación de dos símbolos de y comercial y el nombre del marco en el campo de parámetro. En el ejemplo siguiente se muestran los parámetros de *comando* típicos. Especifica que se debe iniciar la dirección URL de la *Página* en *el marco frame.*


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



No se llama al evento comando si se está examinando el archivo (reenviado rápido o rápido-invertido).

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Settings. baseURL**](settings-baseurl.md)
</dt> <dt>

[**Settings. defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Settings. invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





