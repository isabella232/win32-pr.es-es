---
description: Cuando el instalador procesa el script de instalación, genera simultáneamente un script de reversión.
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: Revertir acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4ad91f8f94145399d51ed2ef53999ab0a91d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908436"
---
# <a name="rollback-custom-actions"></a>Revertir acciones personalizadas

Cuando el instalador procesa el script de instalación, genera simultáneamente un script de reversión. Además del script de reversión, el instalador guarda una copia de todos los archivos que elimina durante la instalación. Estos archivos se conservan en un directorio oculto del sistema. Una vez completada la instalación, se eliminan el script de reversión y los archivos guardados. Si una instalación no se realiza correctamente, el instalador intenta revertir los cambios realizados durante la instalación y restaurar el estado original del equipo.

Aunque las acciones personalizadas que programan las operaciones del sistema mediante la inserción de filas en la tabla de la base de datos se invierten mediante una reversión de la instalación, las acciones personalizadas que cambian el sistema directamente o que emiten comandos a otros servicios del sistema no se pueden invertir siempre mediante una reversión. Una acción de reversión personalizada es una acción que el instalador solo ejecuta durante una reversión de la instalación y su finalidad es invertir una acción personalizada que ha realizado cambios en el sistema.

Una acción personalizada rollback es un tipo de [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), porque su ejecución se aplaza cuando se invoca durante la secuencia de instalación. Difiere de una acción personalizada diferida normal en que solo se ejecuta durante una reversión. Una acción personalizada rollback debe preceder siempre A la acción personalizada diferida que se revierte en la secuencia de acción. Una acción personalizada rollback también debe controlar el caso en el que se interrumpe la acción personalizada diferida en medio de la ejecución. Por ejemplo, si el usuario presiona el botón Cancelar mientras se ejecutaba la acción personalizada.

Tenga en cuenta que las acciones personalizadas de reversión no se pueden ejecutar de forma asincrónica. Vea [acciones personalizadas sincrónicas y asincrónicas](synchronous-and-asynchronous-custom-actions.md).

El complemento de una acción personalizada rollback es una [acción personalizada commit](commit-custom-actions.md). El instalador ejecuta una acción personalizada commit durante la secuencia de instalación, copia la acción personalizada en el script de reversión, pero no ejecuta la acción durante la reversión.

Tenga en cuenta que es posible que una acción personalizada de reversión no pueda quitar todos los cambios realizados por las acciones de confirmación personalizadas. Aunque el instalador escribe las acciones personalizadas de reversión y confirmación en el script de reversión, la confirmación de acciones personalizadas solo se ejecuta después de que el instalador haya procesado correctamente el script de instalación. La confirmación de acciones personalizadas son las primeras acciones que se ejecutan en el script de reversión. Si se produce un error en una acción personalizada commit, el instalador inicia la reversión, pero solo puede revertir las operaciones ya escritas en el script de reversión. Esto significa que, dependiendo de la acción personalizada commit, es posible que una operación de reversión no pueda deshacer los cambios realizados por la acción. Puede omitir los errores en confirmar acciones personalizadas mediante la creación de la acción personalizada para omitir los códigos de retorno.

Cuando el instalador ejecuta una acción personalizada de reversión, el único parámetro de modo que se establecerá es MSIRUNMODE \_ ROLLBACK. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obtener una descripción de los parámetros de modo de ejecución.

Se puede especificar una acción de reversión personalizada agregando una marca de opción al campo de tipo de la [tabla CustomAction](customaction-table.md). Consulte [acción personalizada In-Script opciones de ejecución](custom-action-in-script-execution-options.md) para la marca de opción que designa una acción personalizada de reversión.

Las acciones personalizadas de reversión y confirmación no se ejecutan cuando la reversión está deshabilitada. Si un autor de paquetes requiere estos tipos de acciones personalizadas para una instalación adecuada, deben usar la propiedad [**RollbackDisabled**](rollbackdisabled.md) en una condición que impida que la instalación continúe cuando la reversión está deshabilitada. Para obtener información sobre cómo deshabilitar la reversión [, vea instalación de reversión (Windows Installer)](rollback-installation.md).

 

 



