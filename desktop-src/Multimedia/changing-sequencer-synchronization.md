---
title: Cambiar la sincronización del secuenciador
description: Cambiar la sincronización del secuenciador
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371707"
---
# <a name="changing-sequencer-synchronization"></a>Cambiar la sincronización del secuenciador

> [!NOTE]
> La comunicación sin sesgos de Microsoft admite un entorno diverso e inclusario.  Dentro de este documento, hay referencias a la palabra "subordinada". La Guía de estilo de Microsoft [Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra excluyente.  Esta redacción se usa, ya que actualmente es la que se usa en el software. Por coherencia, este documento contiene esta palabra. Cuando esta palabra se quite del software, corregiremos este documento para que esté alineado.

Para cambiar el modo de sincronización de un dispositivo secuenciador, use el mensaje de comando [**MCI \_ SET**](mci-set.md) con las marcas MCI SEQ SET MASTER y \_ \_ \_ MCI \_ SEQ \_ SET \_ SLAVE. Dos miembros de la estructura [**MCI \_ SEQ \_ SET \_ PARMS,**](mci-seq-set-parms.md) **dwMaster** y **dwMastere,** se usan para especificar los modos de sincronización maestro y subordinado.

El modo de sincronización maestra controla la información de sincronización enviada por el secuenciador a un puerto de salida. A continuación se encuentran las constantes para el **miembro dwMaster** y sus modos de sincronización maestros correspondientes.



| Constante        | Modo de sincronización                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ SEQ \_ MIDI  | Sincronización de MIDI. Enviar información de tiempo al puerto de salida mediante mensajes de reloj de control de tiempo DE MIDI.   |
| MCI \_ SEQ \_ SMPTE | Sincronización de SMPTE. Enviar información de tiempo al puerto de salida mediante mensajes de fotogramas de trimestre de MIDI. |
| MCI \_ SEQ \_ NONE  | Sin sincronización. No enviar información de tiempo.                                                  |



 

El modo de sincronización subordinado controla dónde obtiene el secuenciador su información de tiempo para reproducir un archivo MIDI. A continuación se encuentran las constantes para el **miembro dwAltere** y sus modos de sincronización subordinados correspondientes.



| Constante        | Modo de sincronización                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ARCHIVO MCI \_ \_ SEQ  | Sincronización de archivos. Obtenga información de tiempo del archivo MIDI.                                                                                       |
| MCI \_ SEQ \_ MIDI  | Sincronización de MIDI. Obtenga información de tiempo del puerto de entrada mediante mensajes de reloj de control de tiempo DE MIDI.                                                     |
| MCI \_ SEQ \_ SMPTE | Sincronización de SMPTE. Obtenga información de tiempo del puerto de entrada mediante mensajes de fotogramas de trimestre de MIDI.                                                   |
| MCI \_ SEQ \_ NONE  | Sin sincronización. Obtenga información de tiempo solo de los comandos MCI e ignore la información de tiempo (como los cambios de tempo) que se encuentran en el archivo MIDI. |



 

> [!Note]  
> Actualmente, para la sincronización maestra, el secuenciador MCI MIDI solo admite el modo Sin sincronización (MCI \_ SEQ \_ NONE). Para la sincronización subordinada, solo admite el modo de sincronización de archivos (MCI SEQ FILE) y el modo Sin sincronización \_ \_ (MCI \_ SEQ \_ NONE).

 

 

 




