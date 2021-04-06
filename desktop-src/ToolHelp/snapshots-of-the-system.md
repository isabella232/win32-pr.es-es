---
title: Instantáneas del sistema
description: Las instantáneas son el núcleo de las funciones de ayuda de la herramienta. Una instantánea es una copia de solo lectura del estado actual de una o varias de las listas siguientes que residen en los procesos, subprocesos, módulos y montones de memoria del sistema.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904700"
---
# <a name="snapshots-of-the-system"></a>Instantáneas del sistema

Las instantáneas son el núcleo de las funciones de ayuda de la herramienta. Una instantánea es una copia de solo lectura del estado actual de una o varias de las listas siguientes que residen en la memoria del sistema: procesos, subprocesos, módulos y montones.

Los procesos que usan funciones de ayuda de herramientas de tienen acceso a estas listas desde instantáneas en lugar de hacerlo directamente desde el sistema operativo. Las listas de la memoria del sistema cambian cuando se inician y finalizan los procesos, se crean y destruyen los subprocesos, los módulos ejecutables se cargan y descargan de la memoria del sistema, y se crean y destruyen los montones. El uso de información de una instantánea evita incoherencias. De lo contrario, los cambios en una lista podrían provocar que un subproceso recorra la lista incorrectamente o cause una infracción de acceso (un error de GP). Por ejemplo, si una aplicación atraviesa la lista de subprocesos mientras se crean o finalizan otros subprocesos, la información que utiliza la aplicación para atravesar la lista de subprocesos podría quedar obsoleta y podría provocar un error en la aplicación que atraviesa la lista.

Para tomar una instantánea de la memoria del sistema, utilice la función [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) . Puede controlar el contenido de una instantánea especificando uno o varios de los siguientes valores al llamar a esta función:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Los valores de **TH32CS \_ SNAPHEAPLIST** y **TH32CS \_ SNAPMODULE** son específicos del proceso. Cuando se especifican estos valores, se incluyen en la instantánea las listas del montón y del módulo del proceso especificado. Si especifica cero como identificador de proceso, se utiliza el proceso actual. El valor de **\_ SNAPTHREAD de TH32CS** siempre crea una instantánea en todo el sistema aunque se pase un identificador de proceso a [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).

Para enumerar el estado del montón o del módulo para todos los procesos, especifique el valor de **\_ SNAPALL de TH32CS** y el identificador de proceso del proceso actual. A continuación, para cada proceso adicional de la instantánea, llame de nuevo a [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , especificando su identificador de proceso y el valor de **TH32CS \_ SNAPHEAPLIST** o **TH32CS \_ SNAPMODULE** .

Puede recuperar un código de estado de error extendido para [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) mediante la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Cuando el proceso termine de usar una instantánea, destruya con la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si no destruye una instantánea, el proceso perderá memoria hasta que se cierre, momento en el que el sistema reclama la memoria.

> [!Note]  
> El identificador de la instantánea actúa como un identificador de archivo y está sujeto a las mismas reglas en relación con los procesos y subprocesos en los que se puede usar. Para especificar que el identificador sea heredable, cree la instantánea mediante el valor de **\_ herencia TH32CS** .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tomar una instantánea y ver los procesos](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 