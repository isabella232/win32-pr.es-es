---
title: Propiedad SRStatus
description: Propiedad SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7cc079c79b3539fa5ad90da4f45907236f19d3b841cf580142446b230ff7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975685"
---
# <a name="srstatus-property"></a>Propiedad SRStatus

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve si se puede iniciar la entrada de voz para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). SRStatus_*



| Value | Descripción                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Las condiciones admiten la entrada de voz.                                                                                                                                                                                                          |
| 1     | No hay ningún dispositivo de entrada de audio disponible en este sistema. (Tenga en cuenta que esto no detecta si un micrófono está instalado; solo puede detectar si el usuario tiene una tarjeta de sonido habilitada para entrada correctamente instalada con un controlador de trabajo). |
| 2     | Otro cliente es el cliente activo de este carácter o el carácter actual no está en la parte superior.                                                                                                                                           |
| 3     | El canal de entrada o salida de audio está ocupado actualmente, una aplicación usa audio.                                                                                                                                                       |
| 4     | Se produjo un error no especificado en el proceso de inicialización del subsistema de reconocimiento de voz. Esto incluye la posibilidad de que no haya ningún motor de voz disponible que coincida con la configuración de idioma del carácter.                          |
| 5     | El usuario ha deshabilitado la entrada de voz en opciones avanzadas de caracteres.                                                                                                                                                                     |
| 6     | Se produjo un error al comprobar el estado del audio, pero el sistema no devolvió la causa del error.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve las condiciones necesarias para admitir la entrada de voz, incluido el estado del dispositivo de audio. Puede comprobar esta propiedad antes de llamar al método [**Listen**](listen-method.md) para asegurarse de que se ha hecho correctamente.

Cuando la entrada de voz está habilitada en la hoja de propiedades del Agente (Opciones avanzadas de caracteres), al consultar esta propiedad se cargará el motor asociado, si aún no está cargado, y se iniciarán los servicios de voz. Es decir, la clave De escucha está disponible y la sugerencia de escucha se puede mostrar automáticamente. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en Opciones avanzadas de caracteres). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia los servicios de voz.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Método Listen**](listen-method.md)


 

 




