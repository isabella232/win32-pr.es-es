---
description: 'Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia interno: TIC.'
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074345"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe es una utilidad de línea de comandos que puede ejecutar un conjunto de evaluadores de coherencia [interno: ICE](internal-consistency-evaluators-ices.md).

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

Para obtener más información sobre los TIC y el archivo CSV, vea [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Sintaxis

**Msival2** *{database}{ARCHIVO DE DESTINO} \[ \] \[ -f -l {logfile} \] \[ -i {ICE Id} \[ :{ICE \] \] Id}...*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msival2.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtre todos los mensajes informativos de los resultados mostrados. Se muestran todos los demás tipos de mensajes.                                                                                                                                                                                              |
| -i     | Ejecute solo los TIC enumerados en la línea de comandos en el orden especificado. Cada acción personalizada de ICE debe aparecer tal como aparece en la [tabla CustomAction](customaction-table.md) del archivo CSV. Si se omite esta opción, la herramienta ejecuta el conjunto predeterminado de TIC especificados por el autor del archivo CSV. |
| -l     | Escriba los resultados en el archivo especificado. El archivo no debe existir. Si el archivo existe, no se sobrescribe.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



