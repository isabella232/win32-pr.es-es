---
title: Cambiar la sincronización del secuenciador
description: Cambiar la sincronización del secuenciador
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105653113"
---
# <a name="changing-sequencer-synchronization"></a>Cambiar la sincronización del secuenciador

> [!NOTE]
> Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.  Dentro de este documento, hay referencias a la palabra ' Slave '. La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.  Este texto se utiliza como es el que se utiliza actualmente en el software. Para mantener la coherencia, este documento contiene esta palabra. Cuando se quita esta palabra del software, se corregirá este documento para que esté alineado.

Para cambiar el modo de sincronización de un dispositivo Sequencer, use el mensaje del comando [**\_ set MCI**](mci-set.md) con las marcas de MCI \_ Seq \_ set \_ Master y MCI \_ Seq \_ set \_ Slave. Dos miembros de la estructura de [**parms de MCI \_ Seq \_ set \_**](mci-seq-set-parms.md) , **dwMaster** y **dwSlave**, se usan para especificar los modos de sincronización maestro y subordinado.

El modo de sincronización maestra controla la información de sincronización enviada por Sequencer a un puerto de salida. A continuación se muestran las constantes del miembro **dwMaster** y sus modos de sincronización maestra correspondientes.



| Constante        | Modo de sincronización                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ Seq \_ MIDI  | Sincronización MIDI. Enviar información de temporización al puerto de salida mediante mensajes de reloj de temporización de MIDI.   |
| MCI \_ Seq \_ SMPTE | Sincronización SMPTE. Enviar información de temporización al puerto de salida mediante mensajes MIDI Quarter-frame. |
| MCI \_ Seq \_ ninguno  | Sin sincronización. No enviar información de control de tiempo.                                                  |



 

El modo de sincronización subordinado controla dónde el secuenciador obtiene la información de tiempo para reproducir un archivo MIDI. A continuación se enumeran las constantes para el miembro **dwSlave** y sus modos de sincronización subordinados correspondientes.



| Constante        | Modo de sincronización                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_archivo de SEQ de MCI \_  | Sincronización de archivos. Obtiene la información de tiempo del archivo MIDI.                                                                                       |
| MCI \_ Seq \_ MIDI  | Sincronización MIDI. Obtiene la información de tiempo del puerto de entrada mediante mensajes de reloj de temporización de MIDI.                                                     |
| MCI \_ Seq \_ SMPTE | Sincronización SMPTE. Obtenga información de control de tiempo desde el puerto de entrada mediante mensajes MIDI Quarter-frame.                                                   |
| MCI \_ Seq \_ ninguno  | Sin sincronización. Obtiene la información de tiempo de los comandos MCI únicamente y omite la información de tiempo (por ejemplo, los cambios de Temp.) que se encuentran en el archivo MIDI. |



 

> [!Note]  
> Actualmente, para la sincronización maestra, el secuenciador MIDI de MCI solo admite el modo sin sincronización (MCI \_ Seq \_ None). Para la sincronización subordinada, solo admite el modo de sincronización de archivos ( \_ archivo de sec. SEQ \_ ) y el modo sin sincronización (MCI \_ Seq \_ ninguno).

 

 

 




