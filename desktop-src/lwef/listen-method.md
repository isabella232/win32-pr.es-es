---
title: Listen (método)
description: Listen (método)
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077623"
---
# <a name="listen-method"></a>Listen (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Activa el modo de escucha (reconocimiento de voz) durante un período de tiempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres * * * * ("*** CharacterID * * *").* *  *Estado* de escucha



| Parte    | Descripción                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estado* | Obligatorio. Valor booleano que determina si se activa o desactiva el modo de escucha. **True** Activa el modo de escucha. <br/> **False** Desactiva el modo de escucha.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al establecer este método en **true** , se habilita el modo de escucha (activa el reconocimiento de voz) durante un período de tiempo fijo (10 segundos). Aunque no se puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera. Si usted (u otro cliente) establece correctamente el modo de escucha en e intenta establecer esta propiedad en **true** antes de que expire el tiempo de espera, el método se ejecuta correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha está activado porque el usuario está presionando la clave de escucha, el método se ejecuta correctamente, pero se omite el tiempo de espera y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.

Este método solo se realiza correctamente cuando lo llama el cliente de entrada-activo y si se han iniciado los servicios de voz. Para asegurarse de que se han iniciado los servicios de voz, consulte o establezca el valor de [**SRModeID**](srmodeid-property.md) o establezca la configuración de [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object) antes de llamar a **Listen** ; de lo contrario, se producirá un error en el método. Para detectar el éxito de este método, llámelo como una función y devolverá un valor booleano que indica si el método se realizó correctamente.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



También se produce un error en el método si el usuario presiona la tecla de escucha e intenta establecer **Listen** en **false**. Sin embargo, si el usuario ha liberado la clave de escucha y el modo de escucha no ha agotado el tiempo de espera, se realizará correctamente.

La **escucha** también produce un error si no hay ningún motor de voz compatible disponible que coincida con la configuración de [**LanguageID**](languageid-property.md) del carácter, el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades del agente de Microsoft o el dispositivo de audio está ocupado.

Cuando se establece correctamente este método en **true**, el servidor desencadena el evento [**ListenStart**](listenstart-event.md) . El servidor envía [**ListenComplete**](listencomplete-event.md) cuando se completa el tiempo de espera de modo de escucha o cuando se establece la **escucha** en **false**.

Este método no llama automáticamente a [**detener**](stop-method.md) y reproducir una animación de estado de escucha como el servidor cuando se presiona la tecla de escucha. Esto le permite determinar si desea interrumpir la animación actual mediante la animación [**ListenStart**](listenstart-event.md) llamando a **Stop** y reproduciendo su propia animación adecuada. Sin embargo, el servidor llama a **Stop** y reproduce una animación de estado de audición cuando se detecta un utterance de usuario.

## <a name="see-also"></a>Consulte también

[**Propiedad LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)


 

