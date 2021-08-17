---
description: El componente Lector de Windows diario de Microsoft proporciona acceso de lectura mediante programación a los archivos en formato de diario.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Uso del componente de lector de diario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41559ac31ff081ecb810b0fe6e82ce1107ed87dae897cc7e6b8be4569e9b78f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449207"
---
# <a name="using-the-journal-reader-component"></a>Uso del componente de lector de diario

El componente Lector de Windows diario de Microsoft proporciona acceso de lectura mediante programación a los archivos en formato de diario.

## <a name="component-overview"></a>Información general sobre componentes

Los archivos de diario tienen la extensión de archivo .jnt. Este componente simple toma una secuencia que contiene un archivo .jnt y devuelve una secuencia que contiene el contenido del archivo en formato XML. El XML devuelto por el componente se ajusta al esquema del Lector de notas del diario. Este esquema se documenta en Referencia [de esquema de lector de diario](journal-reader-schema-reference.md).

El componente no proporciona la capacidad de escribir archivos .jnt.

El componente está disponible en versiones administradas y no administradas. El componente no administrado está disponible en la biblioteca journal.dll de vínculos dinámicos (DLL). La versión administrada está en el ensamblado Microsoft.Ink.Journal.dll (para redistribuir a Windows XP Tablet PC Edition o Windows Vista) o Microsoft.Ink.dll.

> [!IMPORTANT]
>
> A partir Windows 10, versión 1607, journal.dll no se incluye en el Windows operativo. Esa biblioteca debe considerarse en desuso u obsoleta y no debe usarse.

 

### <a name="assembly-changes-of-note"></a>Cambios de nota del ensamblado

Es importante tener en cuenta algunos cambios en el ensamblado que contiene el componente Lector de notas del diario que se produjeron entre la versión publicada junto con la versión 1.7 del Kit para desarrolladores de tabletas y la versión que se incluye en el sistema operativo Windows Vista.

La versión 1.7 del componente lector, que se puede redistribuir a Windows XP o Windows Vista, se encuentra en un ensamblado denominado Microsoft.Ink.Journal.dll. El componente lector se distribuye en Windows Vista, pero se ha integrado en el ensamblado Microsoft.Ink.dll principal. Esto significa que las aplicaciones que usan el ensamblado 1.7 deben redistribuir ese ensamblado con su configuración.

## <a name="using-the-component"></a>Usar el componente

El componente Lector de notas del diario es útil para extraer los datos de entrada manuscrita y otra información sobre el archivo de un archivo de diario.

### <a name="com"></a>COM

El componente COM lector de notas del diario se encuentra en el archivo Journal.dll, que se instala y registra al descargar y ejecutar el archivo de instalación del Lector de notas del diario.

El componente COM no admite la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

### <a name="managed"></a>Administrado

El componente administrado lector de notas de diario está en el Microsoft.Ink.JournalReader.dll ensamblado. Este ensamblado se instala y registra en la caché global de ensamblados al ejecutar el archivo de instalación del Lector de notas del diario.

Agregue una referencia al ensamblado para usarla en el proyecto administrado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IJournalReader (interfaz)**](ijournalreader.md)
</dt> <dt>

[Referencia del esquema del lector de diario](journal-reader-schema-reference.md)
</dt> </dl>

 

 
