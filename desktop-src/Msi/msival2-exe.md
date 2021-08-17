---
description: 'Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia internos: ICE.'
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ed1228413d5b2fab0dfab79ea4546a9d15e74c8c62e9b1ca9751699f469854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943882"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia [internos: ICEs](internal-consistency-evaluators-ices.md).

Esta herramienta solo está disponible en los componentes del [SDK Windows para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md)

Para obtener más información sobre los TIC y el archivo CSV, vea [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Syntax

**Msival2** *{database}{ARCHIVO DE PAGINA} \[ \] \[ -f -l {logfile} \] \[ -i {ICE Id} \[ :{ICE \] \] Id}...*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msival2.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guion.



| Opción | Descripción                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtre todos los mensajes informativos de los resultados mostrados. Se muestran todos los demás tipos de mensajes.                                                                                                                                                                                              |
| -i     | Ejecute solo los ICE enumerados en la línea de comandos en el orden especificado. Cada acción personalizada de ICE debe aparecer tal como aparece en la [tabla CustomAction](customaction-table.md) del archivoPARENT. Si se omite esta opción, la herramienta ejecuta el conjunto predeterminado de TIC especificados por el autor del archivo CSV. |
| -l     | Escriba los resultados en el archivo especificado. El archivo no debe existir. Si el archivo existe, no se sobrescribe.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



