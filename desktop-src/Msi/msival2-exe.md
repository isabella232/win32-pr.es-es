---
description: Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia internos, CIEM.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279337"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de [evaluadores de coherencia internos, CIEM](internal-consistency-evaluators-ices.md).

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Para obtener más información acerca del ICEs y el archivo CUB, consulte [uso de evaluadores de coherencia internos](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Sintaxis

**Msival2** *{Database} {Cub file} \[ -f \] \[ -l {logfile} \] \[ -i {Ice ID} \[ : {Ice ID}... \] \]*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msival2.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtre todos los mensajes informativos de los resultados mostrados. Se muestran todos los demás tipos de mensajes.                                                                                                                                                                                              |
| -i     | Ejecute únicamente el ICEs indicado en la línea de comandos en el orden especificado. Cada acción personalizada ICE debe aparecer tal como aparece en la [tabla CustomAction](customaction-table.md) del archivo Cub. Si se omite esta opción, la herramienta ejecuta el conjunto predeterminado de CIEM especificado por el autor del archivo CUB. |
| -l     | Escribe los resultados en el archivo especificado. El archivo no debe existir todavía. Si el archivo existe, no se sobrescribe.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



