---
title: Método Listen
description: Método Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248631"
---
# <a name="listen-method"></a>Método Listen

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Activa el modo de escucha (reconocimiento de voz) durante un período de tiempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters*")("**_CharacterID_*_"). Estado de_ *  *escucha*



| Parte    | Descripción                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estado* | Necesario. Valor booleano que determina si se debe activar o desactivar el modo de escucha. **True** Activa el modo de escucha. <br/> **False** Desactiva el modo de escucha.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Establecer este método en **True habilita** el modo de escucha (activa el reconocimiento de voz) durante un período fijo de tiempo (10 segundos). Aunque no puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera. Si usted (u otro cliente) ha establecido correctamente el modo de escucha en e intenta establecer esta propiedad en **True** antes de que expire el tiempo de espera, el método se realiza correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha está en porque el usuario presiona la tecla Escuchando, el método se realiza correctamente, pero se omite el tiempo de espera y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.

Este método solo se realiza correctamente cuando lo llama el cliente activo de entrada y si se han iniciado los servicios de voz. Para asegurarse de que se han iniciado los servicios de [](voice-property.md) voz, consulte o establezca [**srModeID**](srmodeid-property.md) o establezca la configuración de voz para un comando antes de llamar [**a**](/windows/desktop/lwef/the-command-object) **Listen;** de lo contrario, se producirá un error en el método. Para detectar el éxito de este método, llámelo como una función y devolverá un valor booleano que indica si el método se ha correcto.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



El método también produce un error si el usuario presiona la tecla Listening e intenta establecer **Listen** en **False.** Sin embargo, si el usuario ha liberado la clave de escucha y el modo de escucha no ha pasado el tiempo de espera, se realizará correctamente.

**La** escucha también produce un error si no hay ningún motor de voz compatible disponible que coincida con la configuración [**de LanguageID**](languageid-property.md) del carácter, si el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades de Microsoft Agent o si el dispositivo de audio está ocupado.

Cuando se establece correctamente este método en **True,** el servidor desencadena el [**evento ListenStart.**](listenstart-event.md) El servidor envía [**ListenComplete**](listencomplete-event.md) cuando se completa el tiempo de espera del modo de escucha o cuando se **establece Escuchar** en **False.**

Este método no llama automáticamente a [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed. Esto le permite determinar si se interrumpe la animación actual mediante la animación [**ListenStart**](listenstart-event.md) mediante una llamada a **Stop** y la reproducción de su propia animación adecuada. Sin embargo, el servidor llama a **Stop y** reproduce una animación de estado de audiencia cuando se detecta una expresión del usuario.

## <a name="see-also"></a>Consulte también

[**Propiedad LanguageID,**](languageid-property.md) [**evento ListenComplete,**](listencomplete-event.md) [**evento ListenStart**](listenstart-event.md)


 

