---
title: Instantáneas del sistema
description: Las instantáneas se encuentran en el núcleo de las funciones de ayuda de la herramienta. Una instantánea es una copia de solo lectura del estado actual de una o varias de las listas siguientes que residen en procesos de memoria del sistema, subprocesos, módulos y montones.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30dde3a4383bf56bdef46c59c55611ffe9b22a7a201abb4f0f11af85594c4f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137418"
---
# <a name="snapshots-of-the-system"></a>Instantáneas del sistema

Las instantáneas se encuentran en el núcleo de las funciones de ayuda de la herramienta. Una instantánea es una copia de solo lectura del estado actual de una o varias de las listas siguientes que residen en la memoria del sistema: procesos, subprocesos, módulos y montones.

Los procesos que usan funciones de ayuda de herramientas acceden a estas listas desde instantáneas en lugar de directamente desde el sistema operativo. Las listas de la memoria del sistema cambian cuando los procesos se inician y finalizan, se crean y destruyen subprocesos, los módulos ejecutables se cargan y descargan de la memoria del sistema y se crean y destruyen montones. El uso de información de una instantánea evita incoherencias. De lo contrario, los cambios en una lista podrían provocar que un subproceso atravesara incorrectamente la lista o provocara una infracción de acceso (un error de GP). Por ejemplo, si una aplicación recorre la lista de subprocesos mientras se crean o finalizan otros subprocesos, la información que usa la aplicación para recorrer la lista de subprocesos podría quedar obsoleta y podría producir un error para la aplicación que recorre la lista.

Para tomar una instantánea de la memoria del sistema, use la [**función CreateToolhelp32Snapshot.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) Puede controlar el contenido de una instantánea especificando uno o varios de los valores siguientes al llamar a esta función:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

Los **valores TH32CS \_ SNAPHEAPLIST** y **TH32CS \_ SNAPMODULE** son específicos del proceso. Cuando se especifican estos valores, las listas de montón y módulo del proceso especificado se incluyen en la instantánea. Si especifica cero como identificador del proceso, se usa el proceso actual. El **valor TH32CS \_ SNAPTHREAD** siempre crea una instantánea de todo el sistema incluso si se pasa un identificador de proceso a [**CreateToolhelp32Snapshot.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)

Para enumerar el estado del montón o módulo para todos los procesos, especifique el valor **TH32CS \_ SNAPALL** y el identificador de proceso del proceso actual. A continuación, para cada proceso adicional de la instantánea, vuelva a llamar a [**CreateToolhelp32Snapshot,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) especificando su identificador de proceso y el valor **TH32CS \_ SNAPHEAPLIST** o **TH32CS \_ SNAPMODULE.**

Puede recuperar un código de estado de error extendido [**para CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) mediante la [**función GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Cuando el proceso termine de usar una instantánea, destruyéla mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Si no destruye una instantánea, el proceso pierde memoria hasta que se cierra, momento en el que el sistema reclama la memoria.

> [!Note]  
> El identificador de instantánea actúa como un identificador de archivo y está sujeto a las mismas reglas con respecto a los procesos y subprocesos en los que se puede usar. Para especificar que el identificador es heredable, cree la instantánea con el valor INHERIT de **TH32CS. \_**

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tomar una instantánea y ver procesos](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 