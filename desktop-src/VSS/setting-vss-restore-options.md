---
description: Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a los escritores.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Establecer las opciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ca56a516148bcc11a12fc72aaa6941b0436236525c06c63142107bd18b59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122000"
---
# <a name="setting-vss-restore-options"></a>Establecer las opciones de restauración de VSS

Las opciones de restauración permiten a los solicitantes comunicar opciones de restauración personalizadas a los escritores.

## <a name="restore-options"></a>Opciones de restauración

La normalización del formato de las opciones de restauración permite a los escritores y solicitantes controlar las solicitudes personalizadas comunes. El solicitante establece las opciones de restauración llamando al método [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) hasta una vez por componente seleccionado para copia de seguridad antes de llamar al método [**IVssBackupComponents::P restore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) La cadena que se pasa en el *parámetro wszRestoreOptions* al **método SetRestoreOptions** puede contener varios valores, como se describe a continuación.

## <a name="format"></a>Formato

El formato de las opciones de restauración es uno o varios pares de nombre/valor separados por comas y, opcionalmente, el nombre tiene como prefijo el nombre del subcomponente al que se aplica. Los nombres de componente y los nombres de opción no tienen en cuenta mayúsculas de minúsculas. El escritor determina la confidencialidad de mayúsculas y minúsculas de los valores. Por ejemplo:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

En este ejemplo, "Option1" solo se aplica al subcomponente "Child1" y sus descendientes, "Option2" se aplica a todos los componentes y sus descendientes, y "Option3" solo se aplica a los subcomponentes "Child2 Grandchild3" y sus \\ descendientes.

El [**método SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) solo se puede llamar en componentes que se pueden seleccionar para la copia de seguridad, mientras que es posible que los nodos descendientes no se puedan seleccionar para la copia de seguridad, ya que pueden seleccionarse para la restauración.

## <a name="common-restore-options"></a>Opciones comunes de restauración

Estas opciones comunes de restauración se han definido para aumentar la interoperabilidad entre escritores y solicitantes.

-   Autoridad

    La opción "Autoritativa" admite varios valores "Item", pero solo un valor "All".

    Todo este componente es autoritativo.

    ``` syntax
    "Authoritative"="All"
    ```

    Solo el elemento especificado es autoritativo. El escritor define el formato del elemento con nombre. Las designaciones comunes son \* " " para indicar todos los archivos, "..." para indicar todos los archivos y subdirectorios del componente especificado.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Reversión

    Después de restaurar una base de datos, los escritores suelen pasar a través de registros para poner la base de datos al día. En el caso de restauraciones incrementales o diferenciales, el solicitante usa el método [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) para controlar parcialmente el comportamiento de control de registros. Esta opción de restauración permite un control más pormenorizado.

    No revierte los registros.

    ``` syntax
    "Roll Forward"="None"
    ```

    Revierte todos los registros.

    ``` syntax
    "Roll Forward"="All"
    ```

    Revierte los registros hasta el punto especificado. El escritor define el formato del punto especificado.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Nuevo nombre de componente

    Es posible que un sistema de escritura quiera restaurar un componente a un nuevo nombre. Por ejemplo, restaurar una base de datos a un nombre diferente para restaurar un elemento individual; restaurar con el mismo nombre sería para todos los datos Se recomienda que los escritores acepten una ruta de acceso lógica válida y un nombre de componente como valor de esta opción. A menudo se usará con un [*destino dirigido.*](vssgloss-d.md)

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



