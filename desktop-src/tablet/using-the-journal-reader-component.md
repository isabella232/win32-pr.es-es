---
description: El componente lector de notas de Microsoft Windows Journal proporciona acceso de lectura mediante programación a los archivos en formato de diario.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Usar el componente de lector de Journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001111"
---
# <a name="using-the-journal-reader-component"></a>Usar el componente de lector de Journal

El componente lector de notas de Microsoft Windows Journal proporciona acceso de lectura mediante programación a los archivos en formato de diario.

## <a name="component-overview"></a>Información general del componente

Los archivos de diario tienen la extensión de archivo. JNT. Este componente simple toma una secuencia que contiene un archivo. JNT y devuelve una secuencia que contiene el contenido del archivo en formato XML. El XML devuelto por el componente se ajusta al esquema lector de notas de Journal. Este esquema se documenta en [referencia de esquema del lector de diarios](journal-reader-schema-reference.md).

El componente no proporciona la capacidad de escribir archivos. JNT.

El componente está disponible en las versiones administradas y no administradas. El componente no administrado está disponible en la journal.dll biblioteca de vínculos dinámicos (DLL). La versión administrada se encuentra en el Microsoft.Ink.Journal.dll ensamblado (para la redistribución a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partir de Windows 10, versión 1607, journal.dll no se incluye en el sistema operativo Windows. Esa biblioteca debe considerarse en desuso u obsoleta y no debe usarse.

 

### <a name="assembly-changes-of-note"></a>Cambios de ensamblado de nota

Es importante tener en cuenta algunos cambios en el ensamblado que contiene el componente lector de notas de Journal que se produjo entre la versión publicada junto con la versión 1,7 del kit para desarrolladores de Tablet PC y la versión que se incluye en el sistema operativo Windows Vista.

La versión 1,7 del componente lector, que se puede redistribuir a Windows XP o Windows Vista, se encuentra en un ensamblado denominado Microsoft.Ink.Journal.dll. El componente lector se incluye en Windows Vista, pero se ha integrado en el ensamblado principal de Microsoft.Ink.dll. Esto significa que las aplicaciones que usan el ensamblado 1,7 deben redistribuir ese ensamblado con su configuración.

## <a name="using-the-component"></a>Usar el componente

El componente lector de notas de Journal es útil para extraer los datos de tinta y otra información sobre el archivo de un archivo de diario.

### <a name="com"></a>COM

El componente COM lector de notas de Journal está en el archivo Journal.dll, que se instala y registra al descargar y ejecutar el archivo de instalación del lector de notas de Journal.

El componente COM no admite la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

### <a name="managed"></a>Administrado

El componente administrado lector de notas de Journal está en el ensamblado de Microsoft.Ink.JournalReader.dll. Este ensamblado se instala y registra en la caché global de ensamblados al ejecutar el archivo de instalación del lector de notas de Journal.

Agregue una referencia al ensamblado para usarlo en el proyecto administrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IJournalReader**](ijournalreader.md)
</dt> <dt>

[Referencia del esquema del lector de Journal](journal-reader-schema-reference.md)
</dt> </dl>

 

 
