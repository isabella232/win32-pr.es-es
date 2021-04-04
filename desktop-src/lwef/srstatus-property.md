---
title: Propiedad SRStatus
description: Propiedad SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076390"
---
# <a name="srstatus-property"></a>Propiedad SRStatus

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve si se puede iniciar la entrada de voz para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*directivas. ***Caracteres ("*** CharacterID * *"). SRStatus**



| Value | Descripción                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Las condiciones admiten la entrada de voz.                                                                                                                                                                                                          |
| 1     | No hay ningún dispositivo de entrada de audio disponible en este sistema. (Tenga en cuenta que esto no detecta si hay un micrófono instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para la entrada instalada correctamente con un controlador de trabajo). |
| 2     | Otro cliente es el cliente activo de este carácter o el carácter actual no es el nivel superior.                                                                                                                                           |
| 3     | El canal de entrada o salida de audio está ocupado actualmente, una aplicación está utilizando audio.                                                                                                                                                       |
| 4     | Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz. Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.                          |
| 5     | El usuario ha deshabilitado la entrada de voz en las opciones de caracteres avanzadas.                                                                                                                                                                     |
| 6     | Error al comprobar el estado de audio, pero el sistema no ha devuelto la causa del error.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve las condiciones necesarias para admitir la entrada de voz, incluido el estado del dispositivo de audio. Puede comprobar esta propiedad antes de llamar al método [**Listen**](listen-method.md) para garantizar mejor su éxito.

Cuando se habilita la entrada de voz en la hoja de propiedades del agente (opciones avanzadas de caracteres), al consultar esta propiedad se cargará el motor asociado, si aún no está cargado, y se iniciarán los servicios de voz. Es decir, la clave de escucha está disponible y la sugerencia de escucha se puede mostrar automáticamente. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Listen (método)**](listen-method.md)


 

 




