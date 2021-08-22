---
description: A veces resulta útil hacer copias de seguridad y restaurar solo secciones de archivos. VSS proporciona mecanismos de archivo parciales que, si los solicitantes lo admiten, permiten a los escritores especificar copias de seguridad y restauraciones de archivos parciales.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Trabajar con archivos parciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1aa2623788cc97d62c88d52ec7096829adc350e1d420e92cea12b8dd64d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590459"
---
# <a name="working-with-partial-files"></a>Trabajar con archivos parciales

A veces resulta útil hacer copias de seguridad y restaurar solo secciones de archivos. VSS proporciona [*mecanismos de archivo*](vssgloss-p.md) parciales que, si los solicitantes lo admiten, permiten a los escritores especificar copias de seguridad y restauraciones de archivos parciales.

Las operaciones de archivos parciales suelen ser de mayor uso para los escritores que mantienen archivos muy grandes, solo una pequeña fracción de las cuales cambian entre las operaciones de copia de seguridad. En este caso, con frecuencia resulta útil copiar solo esa sección que cambió a medios de copia de seguridad. Por esta razón, las operaciones de archivos parciales se suelen usar, pero no exclusivamente, para admitir operaciones incrementales de copia de seguridad y restauración.

Si un escritor desea implementar una operación de archivo parcial, usa [**CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) para determinar si el solicitante con el que está trabajando admite la operación.

Si el solicitante admite operaciones de archivos parciales y agrega el componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo) al documento Componentes de copia de seguridad, un escritor indica qué secciones del archivo se deben guardar (normalmente mientras se controla un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [*PostSnapshot)*](vssgloss-p.md) mediante una llamada a [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Además de una ruta de acceso y un nombre de archivo, el escritor proporciona el intervalo, información de metadatos opcional a [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

La información del intervalo se proporciona como una cadena que contiene cualquiera de las siguientes opciones:

-   Pares de desplazamientos en el archivo del que se va a realizar una copia de seguridad (en bytes) y la longitud de la sección de la que se va a realizar una copia de seguridad (en bytes), el desplazamiento y la longitud separados por dos puntos y cada par separado por una coma, por ejemplo, *Offset1***:**_Length1_*_,_* *Offset2***:**_Length2_.

    Cada valor es un entero de 64 bits (en formato hexadecimal o decimal) que especifica un desplazamiento de bytes y una longitud en bytes, respectivamente.

-   Ruta de acceso completa, incluido el nombre de archivo, en el sistema actual de un archivo de intervalos binarios que contiene lo siguiente:
    -   Número (expresado como un entero de 64 bits) de intervalos de archivos distintos contenidos en el archivo
    -   Cada intervalo se expresa como un par de enteros de 64 bits: el primer miembro del par es el desplazamiento en el archivo del que se va a realizar la copia de seguridad (en bytes) y el segundo miembro es la longitud de los datos de los que se va a realizar una copia de seguridad (en bytes).

Si un escritor usa un archivo de intervalos para especificar una operación de archivo parcial, un solicitante debe garantizar que se realice una copia de seguridad de este archivo (aunque el archivo no forme parte necesariamente del conjunto de copia de seguridad predeterminado) o que la información de intervalos se conserve en el medio de copia de seguridad de alguna otra manera. Si no se hace una copia de seguridad de la información del archivo de intervalos, será imposible restaurar el archivo de copia de seguridad parcial.

El sistema de escritura también puede agregar una cadena que contenga metadatos. Estos metadatos pueden estar en un formato específico del escritor porque está pensado para permitir que el escritor valide cualquier restauración futura.

Con esta información, un solicitante compatible puede realizar una copia de seguridad de archivos parcial.

Por ejemplo, considere un archivo grande cuyo encabezado (bytes 64-512) contiene un recuento de registros y otra información actualizada con frecuencia, y cuyos datos más recientes se encontrarán en los últimos 65536 bytes del archivo(bytes 0x1239E8577A a 0x1239E7577A.

Un escritor podría especificar una lista de intervalos como la cadena "**64:448,0x1239E8577A:65536**."

En la restauración y antes de realizar realmente una operación de restauración, un solicitante debe comprobar si algún archivo requiere compatibilidad con archivos parciales.

Para ello, el solicitante recorre primero en iteración los escritores con componentes almacenados en su documento componentes de copia de seguridad mediante [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

A continuación, se usa la interfaz [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) para devolver instancias de la interfaz [**IVssWriterComponentsExt,**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) que proporcionan [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), que permiten al solicitante obtener [**instancias de IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Esto permite a un solicitante obtener información sobre los archivos de copia de seguridad parcial para participar en una restauración mediante [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) para la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo).

Si la operación de archivo parcial se controló mediante un archivo de intervalos, ese archivo debe restaurarse antes de copiar los datos en el disco. Puede ocurrir que el solicitante necesite copiar el archivo de intervalos de nuevo en una nueva ubicación en el disco. En este caso, indica que lo ha hecho a través de [**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

A continuación, el solicitante continúa con la copia de datos en las ubicaciones adecuadas del destino de restauración que ya están en el disco.

Un escritor (mientras se administra un evento [**PostRestore),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) mediante el examen de [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) para los archivos indicados por [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), determina si la operación de archivo parcial se ha realizado correctamente. El sistema de escritura siempre debe intentar comprobar la corrección de esta restauración con la información de desplazamiento y los metadatos incluidos en el documento componentes de copia de seguridad.

Si el solicitante ha tenido que restaurar el archivo de intervalos en una nueva ubicación, VSS actualizará esta información para que la ruta de acceso devuelta por [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) sea correcta.

 

 
