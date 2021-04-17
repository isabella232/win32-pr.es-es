---
description: Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a escritores.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Establecer opciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696969"
---
# <a name="setting-vss-restore-options"></a>Establecer opciones de restauración de VSS

Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a escritores.

## <a name="restore-options"></a>Opciones de restauración

La estandarización del formato de las opciones de restauración permite que escritores y solicitantes controlen las solicitudes personalizadas comunes. Las opciones de restauración las establece el solicitante llamando al método [**ivssbackupcomponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) hasta una vez por cada componente de copia de seguridad seleccionado antes de llamar al método [**ivssbackupcomponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) . La cadena que se pasa en el parámetro *wszRestoreOptions* al método **SetRestoreOptions** puede contener varios valores, tal y como se describe a continuación.

## <a name="format"></a>Formato

El formato de las opciones de restauración, es uno o varios pares de nombre/valor separados por comas, y el nombre se antepone opcionalmente al nombre del subcomponente al que se aplica. Los nombres de componente y de opción no distinguen mayúsculas de minúsculas. El escritor determina la distinción de mayúsculas y minúsculas de los valores. Por ejemplo:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

En este ejemplo, "Opción1" solo se aplica al subcomponente "Child1" y a sus descendientes, "opción2" se aplica a todos los componentes y sus descendientes, y "Option3" solo se aplica a los \\ subcomponentes "Child2 Grandchild3" y a sus descendientes.

Solo se puede llamar al método [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) en los componentes que se pueden seleccionar para la copia de seguridad, mientras que los nodos descendientes no se pueden seleccionar para la copia de seguridad, pueden seleccionarse para la restauración.

## <a name="common-restore-options"></a>Opciones de restauración comunes

Estas opciones de restauración comunes se han definido para aumentar la interoperabilidad entre escritores y solicitantes.

-   Restaur

    La opción "autoritativa" admite varios valores "Item", pero solo un valor "All".

    Todo este componente es autoritativo.

    ``` syntax
    "Authoritative"="All"
    ```

    Solo el elemento especificado es autoritativo. El escritor define el formato del elemento con nombre. Las designaciones comunes son " \* " para indicar todos los archivos, "..." para indicar todos los archivos y subdirectorios del componente especificado.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Puesta al día

    Después de restaurar una base de datos, los escritores normalmente se ponen al día a través de los registros para actualizar la base de datos. En el caso de las restauraciones incrementales o diferenciales, el solicitante usa el método [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) para controlar parcialmente el comportamiento de control de registros: esta opción de restauración permite un control más granular.

    No revierta los registros.

    ``` syntax
    "Roll Forward"="None"
    ```

    Revertir todos los registros.

    ``` syntax
    "Roll Forward"="All"
    ```

    Desplazarse por los registros hasta el punto especificado. El escritor define el formato del punto especificado.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Nuevo nombre de componente

    Es posible que un escritor desee restaurar un componente a un nuevo nombre. Por ejemplo, restaurar una base de datos a un nombre diferente para restaurar un elemento individual; al restaurar al mismo nombre, todos los datos recomendamos que los escritores acepten una ruta de acceso lógica y un nombre de componente válidos como valor de esta opción. Esto se suele usar con un [*destino dirigido*](vssgloss-d.md).

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



